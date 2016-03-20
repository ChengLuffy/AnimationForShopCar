- ###用法

1.继承`ShopCarAnimationViewController.h`

1.方法调用`- (void)addProductsAnimation:(UIImageView *)imageView dropToPoint:(CGPoint)dropToPoint isNeedNotification:(BOOL)isNeedNotification;
`
	
```
参数说明
/**
 *  购物车动画，商品图片掉入购物车
 *
 *  @param imageView   掉入购物车的商品图片
 *  @param dropToPoint 掉入位置
 *  @param isNeedNotification 是否有动画结束的通知（用于购物车上的计数加一）
 */

 ```
 注：动画结束用通知的形势发送，如需要，在响应的界面增加收听者
 ```
 [[NSNotificationCenter defaultCenter] addObserver:self selector:@selector(shopCarBadgeValueAdd:) name:@"shopCarAnimationEnd" object:nil];
 ```
 并实现相应方法，在dealloc方法里移除监听者。
 
 - ###CocoaPods
 pod 'CLFAnimationForShopCar', '~> 0.0.2'
