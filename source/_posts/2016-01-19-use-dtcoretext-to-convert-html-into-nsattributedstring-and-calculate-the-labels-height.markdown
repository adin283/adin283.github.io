---
layout: post
title: "使用DTCoreText转换HTML为NSAttributedString"
date: 2015-08-19 17:32:51 +0800
comments: true
categories: 
---
首先引入DTCoreText，推荐使用CocoaPods，因为其实DTCoreText还依赖于DTFoundation，手动引入比较麻烦。
```
 pod 'DTCoreText', '~> 1.6.16'
 
 #import <DTCoreText.h>
```
* 使用DTCoreText转换HTML为NSAttributedString
```objective-c
NSString *htmlString = @"<ol><li>aaaaaa</li><li>bbbbbbbb</li><li>cccccccccc</li></ol>";
NSData *data = [htmlString dataUsingEncoding:NSUTF8StringEncoding];
NSAttributedString *attrString = [[NSAttributedString alloc] initWithHTMLData:data documentAttributes:nil];
```
* 使用生成的NSAttributedString为UILabel的attributedText赋值
```
myLabel.attributedText = attrString;
```
**Error** 其实这样是不行的，会报错lineBreakMode没有啊什么的，虽然生成的是NSAttributedString，但是这个和我们用[[NSAttributedString alloc] init]生成的是不一样的东西，得有容器来装它。

* 使用DTAttributedLabel，初始化和赋值方法如下
```
- (DTAttributedLabel *)descriptionLabel
{
    if (!_descriptionLabel) {
        _descriptionLabel = [[DTAttributedLabel alloc] init];
        _descriptionLabel.numberOfLines = 0;
        _descriptionLabel.lineBreakMode = NSLineBreakByCharWrapping;
    }
    return _descriptionLabel;
}
// 注意这里是attributedString，而不是attributedText
descriptionLabel.attributedString = attrString;
```
* 计算文字高度
```
DTCoreTextLayouter *layouter = [[DTCoreTextLayouter alloc] initWithAttributedString:attrString];
        
CGRect maxRect = CGRectMake(0, 0, 320, CGFLOAT_HEIGHT_UNKNOWN);
NSRange entireString = NSMakeRange(0, [attrString length]);
DTCoreTextLayoutFrame *layoutFrame = [layouter layoutFrameWithRect:maxRect range:entireString];
CGSize sizeNeed = [layoutFrame frame].size;
```

---
参考链接：

1. [DTCoreText on Github](https://github.com/Cocoanetics/DTCoreText)
2. [DTCoreText Programming Guide](https://docs.cocoanetics.com/DTCoreText/docs/Programming Guide.html)