XHFLinearView
=============

iOS LinearView Container and  operate with animations

<img src="http://xuhengfei.com/assets/images/articles/2013-09-28-linearview.png" width="240"/>

##Usage Example

```objective-c
    XHFLinearView *linearView=[[XHFLinearView alloc]initWithFrame:self.view.bounds];
    [self.view addSubview:linearView];
    //init linear view content views
    [linearView.itemSource addObject:XHFLinearViewUnitMake(someView, XHFMarginMake(0, 0, 0, 0))];
    //force layout linear view
    [linearView needLayout];
    //insert a view with animation
    [linearView insertItem:someView margin:XHFMarginMake(0, 0, 0, 0) atIndex:0 withAnimation:XHFLinearItemAnimationFade];
    //replace a view with animation
    [linearView replaceItem:someView withNewItem:newView withAnimation:XHFLinearItemAnimationFade];
    //resize a view with animation
    someView.frame=xxx;
    [linearView needLayoutForItem:someView];
    //remove a view with animation
    [linearView removeItemByIndex:0 withAnimation:XHFLinearItemAnimationFade];
    
```
Checkout the demo project for additional tests and examples.

##Setup Instructions

1.add `src/XHFLinearView.h` and `src/XHFLinearView.m` to your project
