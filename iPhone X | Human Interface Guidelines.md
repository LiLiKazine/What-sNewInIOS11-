# 用户界面指引
### 超视网膜屏
+ 垂直显示时，iPhone X 的宽度与 4.7 寸的 iPhone 6，iPhone7，iPhone 8 一样。但是长度要多 145pt，因此在垂直空间上多出了大概 20% 的空间。

<div class="OV_Screen_Size">
    <img src="https://developer.apple.com/ios/human-interface-guidelines/images/OV_Screen_Size_47.svg" width = "40%"/>
    <img src="https://developer.apple.com/ios/human-interface-guidelines/images/OV_Screen_Size_iPhoneX.svg" width = "40%"/>
</div>


| Portrait dimensions | Landscape dimensions |
| ------------------- | -------------------- |
| 1125px × 2436px (375pt × 812pt @3x) | 2436px × 1125px (812pt × 375pt @3x) |

+ 支持 @3x 大小的图片，推荐使用 pdf 格式。参考 [图片尺寸&分辨率](https://developer.apple.com/ios/human-interface-guidelines/icons-and-images/image-size-and-resolution/)，[自定义图标](https://developer.apple.com/ios/human-interface-guidelines/icons-and-images/custom-icons/)。

### 布局

+ 布局时要确保填充整个屏幕且不被圆角，“刘海” 或下方的 Home 指示条遮蔽。

<div class="OV_Screen">
    <img src="https://developer.apple.com/ios/human-interface-guidelines/images/OV_Fullscreen.svg" width = "40%"/>
    <img src="https://developer.apple.com/ios/human-interface-guidelines/images/OV_Clipping.png" width = "40%"/>
</div>

+ 使用标准库中UI控件 *(eg: navigation bars, tables, collections)* 会自动适应新特性
+ 使用 “自动布局” 并且遵循安全区域和外边距标准，进行自定义布局也不会很难
+ 可以使用 Xcode 中的模拟器预览 app，检测布局问题，但是某些特性，比如色彩显示范围，最好使用真机检测。
+ 为了保证提供全面屏体验，确保背景要延伸到边缘。类似于 ‘table’ ，  ‘collection’ 在垂直滚动布局下，会延续到屏幕的最底端（覆盖 Home 指示条）

<div class="OV_LayoutGuides">
    <img src="https://developer.apple.com/ios/human-interface-guidelines/images/OV_LayoutGuides_Portrait.svg" width = "40%"/>
    <img src="https://developer.apple.com/ios/human-interface-guidelines/images/OV_LayoutGuides_Landscape.svg" width = "40%"/>
</div>

+ 通常，内容应放置在正中间并对称才能在水平和垂直上看上去美观且不被圆角或者 “刘海” 挤压变形或被 Home 指示条遮蔽。最好使用系统提供的标准库中的UI组件以及自动布局对界面进行限制。所有的 app 都应遵循 UIKit 中定义的安全区域和外边距的限制，这样才能确保界面正确的显示。安全区域可以防止内容和状态栏、导航栏、工具栏、标签栏冲突
+ 注意状态栏的高度，在 iPhone X 上，状态栏要比在其它机型上高，而且状态栏不再因为某些后台任务 *(eg: voice recording, location tracking)* 而改变高度。
+ 如果 app 需要隐藏状态栏，在 iPhone X 需要再三思考。iPhone X 提供了比 4.7 寸机型更多的垂直空间，而且状态栏占据的那片区域 app 很难完美适配，而且状态栏也会提供一些很使用的信息，只有在需要展示其它附加信息时在应该隐藏状态栏。

<div class="OV_47">
    <img src="https://developer.apple.com/ios/human-interface-guidelines/images/OV_47_Display.svg" width = "30%" alt="Full-screen 4.7 device image"/>
    <img src="https://developer.apple.com/ios/human-interface-guidelines/images/OV_47_Cropped.svg" width = "30%" alt="Cropping on iPhone X"/>
    <img src="https://developer.apple.com/ios/human-interface-guidelines/images/OV_47_LetterBox.svg" width = "30%" alt="Letterboxing on iPhone X"/>
</div>

<div class="OV_iPhoneX">
    <img src="https://developer.apple.com/ios/human-interface-guidelines/images/OV_iPhoneX_Display.svg" width = "30%" alt = "Full-screen iPhone X image"/>
    <img src="https://developer.apple.com/ios/human-interface-guidelines/images/OV_iPhoneX_Cropped.svg" width = "30%" alt = "Cropping on a 4.7 device"/>
    <img src="https://developer.apple.com/ios/human-interface-guidelines/images/OV_iPhoneX_PillarBox.svg" width = "30%" alt = "Pillarboxing on a 4.7 device"/>
</div>

+ 注意 iPhone X 与 4.7 寸机型有不同的宽高比，重用时要注意重要信息是否被裁剪掉了。
+ 避免在最底部和角落放置交互控件，底部上滑手势用作用来显示 Home 或者切换应用，这些手势有可能会取消你的在这些区域的自定义手势，而角落区域难以触及，在这里使用手势不利于用户体验。
+ 不要掩盖或者特别留意按键显示功能 *(key display feature)* 。不要试图通过放置黑色北京在顶部、底部来掩盖圆角、“刘海” 和 Home 指示条，也不要在这些地方放置不规则图形或者指引文字来引起视觉注意 (意思就是这些地方丑，不要引起用户注意)。
+ 保守的考虑要不要自动隐藏 Home 指示条。允许自动隐藏时，如果用户不触碰屏幕数秒，指示条会渐隐，当用户再次触碰屏幕时会显示。这个功能应该只在长时间观看 *(eg: playing videos, photo slideshows)* 时启用。

更多内容参阅 [适配和布局](https://developer.apple.com/ios/human-interface-guidelines/visual-design/adaptivity-and-layout/)。

### 色彩
+ iPhone X 支持 P3 色彩空间。
+ 使用更广的色域增强视觉效果，见 [色彩管理](https://developer.apple.com/ios/human-interface-guidelines/visual-design/color/#color-management)。

![colorGraphic_wideColor](https://developer.apple.com/ios/human-interface-guidelines/images/colorGraphic_wideColor.svg)

### 手势
+ iPhone X 上使用屏幕边缘手势访问主屏幕、应用切换、通知中心、控制中心。
+ 避免使用与系统冲突的手势。一些沉浸式应用，比如游戏，可能需要自定义优先级大于系统内置的屏幕边缘手势。第一次滑动会调用应用自定义动能，第二次欢动会调用系统功能。这种行为（称为边缘保护）应该保守才用，因为会使用户难以使用系统内置的响应。见 [手势](https://developer.apple.com/ios/human-interface-guidelines/user-interaction/gestures/)。

### 其它的设计考量
+ iPhone X 支持 Face ID 验证。如果应用需要与系统验证功能交互，不要使用 Touch ID。同理，在其它机型上不要使用 Face ID。见[验证](https://developer.apple.com/ios/human-interface-guidelines/user-interaction/authentication/)。
+ 不要重写系统提供的键盘特性。在 iPhone X 上，Emoji/Globe 按键自动出现在键盘上，即使使自定义键盘，应用无法影响这些按钮。见[自定义键盘](https://developer.apple.com/ios/human-interface-guidelines/extensions/custom-keyboards/)。

### 资源
+ 下载 Photoshop 和Sketch 使用的 iPhone X UI 设计模板，在 [资源](https://developer.apple.com/design/resources/#ios-apps)。
