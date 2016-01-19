---
layout: post
title: "UICollectionView align right"
date: 2016-01-20 00:38:31 +0800
comments: true
categories: 
---
参考链接：
http://stackoverflow.com/questions/13588283/how-to-center-align-the-cells-of-a-uicollectionview

方案一：

You can get similar result by performing a transform on the collection view and reverse the flip on its content:

First when creating the UICollectionView I performed a flip on it:


[collectionView_ setTransform:CGAffineTransformMakeScale(-1, 1)];





Then subclass UICollectionViewCell and in here do the same flip on its contentView:


[self.contentView setTransform:CGAffineTransformMakeScale(-1, 1)];





方案二：
https://github.com/mokagio/UICollectionViewRightAlignedLayout
