# 增强现实
Apps can use Apple's augmented reality (AR) technology, ARKit, to deliver immersive, engaging experiences that seamlessly blend realistic virtual objects with the real world. In AR apps, the device's camera is used to present a live, onscreen view of the physical world. Three-dimensional virtual objects are superimposed over this view, creating the illusion that they actually exist. The user can reorient their device to explore the objects from different angles and, if appropriate for the experience, interact with them using gestures and movement.

### 创造引人入胜的应用
+ **通过全面显示吸引用户** Devote as much of the screen as possible to viewing and exploring the physical world and your app's virtual objects. Avoid cluttering the screen with controls and information that diminish the immersive experience.
+ **创造逼真的物品以至于分不清是否是幻觉** Not all AR experiences require realistic virtual objects. Those that do, however, should include objects that appear to inhabit the physical environment in which they're placed. For best results, design detailed 3D assets with lifelike textures and use the information ARKit provides to position objects on detected real-world surfaces, scale objects properly, reflect environmental lighting conditions on virtual objects, cast virtual object shadows on real-world surfaces, and update visuals as the camera's position changes.
+ **考虑物理约束** Bear in mind that people may attempt to use your app in an environment that's not conducive to an optimal AR experience. For example, they may open your app in a location where there isn't much room to move around or there aren't large, flat surface areas. Try to anticipate scenarios that might present challenges, and clearly communicate requirements or expectations to people up front. Consider offering varying sets of features for use in different environments.
+ **注意用户舒适度** Holding a device at a certain distance or angle for a prolonged period of time can be fatiguing. Consider how people must hold their device when using your app, and strive for an enjoyable experience that doesn't cause discomfort. For example, by default, you could place objects at distance that reduces the need to move closer. A game could keep levels short and intermixed with brief periods of downtime.
+ **如果应用需要用户运动，循序渐进的进行引导** In a game, for example, the user shouldn't need to move out of the way to avoid a virtual projectile as soon as they enter AR. Give them time to adapt to the experience first. Then, progressively encourage movement.
+ **注意用户安全** Moving around too much can potentially be dangerous if there are other people or objects nearby. Consider ways of making your app safe to operate. For example, a game could avoid encouraging large or sudden movements.
+ **使用听觉和触觉反馈增强沉浸式体验**  A sound effect or bump sensation is a great way to provide confirmation that a virtual object has come into contact with a physical surface or other virtual object. In an immersive game, background music can help envelop the user in the virtual world. For related guidance, see [Audio](https://developer.apple.com/ios/human-interface-guidelines/user-interaction/audio/) and [Haptic Feedback](https://developer.apple.com/ios/human-interface-guidelines/user-interaction/feedback/#haptics).

<div class="ARKit">
    <img src="https://developer.apple.com/ios/human-interface-guidelines/images/ARKit_11.svg" width = "40%"/>
    <img src="https://developer.apple.com/ios/human-interface-guidelines/images/ARKit_06.svg" width = "40%"/>
</div>

+ **尽可能提供提示** Placing a three-dimensional rotation indicator around an object, for example, is more intuitive than presenting text-based instructions in an overlay. Textual overlay hints may be warranted, however, prior to surface detection or if the user isn't responding to contextual hints.
+ **如果必须显示提示文字，避免使用晦涩的术语** AR is an advanced concept that may be intimidating to some users. To help make it approachable, avoid referring to technical, developer-oriented terms like ARKit, world detection, and tracking. Instead, use friendly, conversational terms that most people will understand.

|                                      DO                                       |                  Don't                   |
| ----------------------------------------------------------------------------- | ---------------------------------------- |
| Unable to find a surface. Try moving to the side or repositioning your phone. | Unable to find a plane. Adjust tracking. |
| Tap a location to place the [name of object to be placed].                    | Tap a plane to anchor an object.         |
| Try turning on more lights and moving around.                                 | Insufficient features.                   |
| Try moving your phone slower. | 	Excessive motion detected. |

+ **避免对AR体验进行不必要的干扰** The environment is analyzed and surfaces are detected each time the user exits and reenters AR. In addition, the phone and camera position has probably changed. As a result, previously placed objects are likely to be repositioned—they may even no longer appear to rest on real-world surfaces. One way to avoid interruptions is to let people make changes to objects and settings without leaving AR. For example, if a user has placed a chair they’re considering purchasing into their living room, they may want to try out other fabric options.

### 进入增强现实
![ARKit](https://developer.apple.com/ios/human-interface-guidelines/images/ARKit_12.svg)
+ **当初始化完成时进行提示并带入用户** An initialization process, during which the surroundings are evaluated, occurs each time your app enters AR. This can take a couple of seconds. To reduce possible confusion and speed up the process, show an indication of activity during initialization and encourage people to explore their surroundings, or to actively look for a surface.

### 放置虚拟物品
<table>
<tr style="width:100%;border-style: none;margin: 1px;padding: 1px">
<td style="width:30%;border-style: none;"><div>
      <img src="https://developer.apple.com/ios/human-interface-guidelines/images/ARKit_Target_1.svg" />
      <p style = "text-align:center">Surface detection indicator</p>
    </div></td>
<td style="width:30%;border-style: none;"> <div>
      <img src="https://developer.apple.com/ios/human-interface-guidelines/images/ARKit_Target_2.svg" />
      <p style = "text-align:center">Object placement indicator</p>
    </div></td>
<td style="width:30%;border-style: none;"><div>
      <img src="https://developer.apple.com/ios/human-interface-guidelines/images/ARKit_Target_3.svg" />
      <p style = "text-align:center">App-specific indicator</p>
    </div></td>
</tr>
</table>

+ **帮助用户理解什么时候应该确定一个表面然后放置物品** A visual indicator is a great way to communicate that surface targeting mode is active. A trapezoidal reticle in the center of the screen, for example, helps people infer that they should find a horizontal, flat surface. Once a surface is targeted, an indicator should change in appearance to suggest that object placement is now possible. Design visual indicators that feel like part of your app experience.
+ **用户放置物品后进行合适的响应** Accuracy is progressively refined (over a very short period of time) during surface detection. If the user taps the screen to place an object, place it immediately using the information that's currently available. Then, once surface detection is complete, subtly refine the object's position. If an object is placed beyond the bounds of the detected surface, gently nudge the object back onto the surface.
+ **避免将物品和检测到的平面边缘进行精确的对齐**  In AR, surface boundaries are approximations that may change as the user's surroundings are further analyzed.

### 用户与虚拟物品交互
<div class="ARKit">
    <img src="https://developer.apple.com/ios/human-interface-guidelines/images/ARKit_User_Interaction_Right.svg" width = "40%"/>
    <img src="https://developer.apple.com/ios/human-interface-guidelines/images/ARKit_User_Interaction_Wrong.svg" width = "40%"/>
</div>

+ **支持在不同平面上进行操作** It's more immersive and intuitive when a user can touch an object onscreen and interact with it directly, rather than interact with separate controls on a different part of the screen. Bear in mind, however, that direct manipulation can sometimes be confusing or difficult when the user is moving around.
+ **允许用户通过标准常用的手势直接与虚拟物品交互**  For example, consider supporting a single-finger drag gesture for moving objects, and a two-finger rotation gesture for spinning objects. For related guidance, see [Gestures](https://developer.apple.com/ios/human-interface-guidelines/user-interaction/gestures/).
+ **总之，保持交互简洁** Touch gestures are inherently two-dimensional, but an AR experience involves the three dimensions of the real world. Consider the following approaches to simplifying user interactions with virtual objects.
<table>
<tr style="width:100%;border-style: none;margin: 1px;padding: 1px">
<td style="width:45%;border-style: none;"><div>
      <img src="https://developer.apple.com/ios/human-interface-guidelines/images/ARKit_10.svg" />
      <p style = "text-align:center">Limit movement to the two-dimensional surface on which the object rests.</p>
    </div></td>
<td style="width:45%;border-style: none;"> <div>
      <img src="https://developer.apple.com/ios/human-interface-guidelines/images/ARKit_09.svg" />
      <p style = "text-align:center">Limit object rotation to a single axis.</p>
    </div></td>
</tr>
</table>

+ **当手势在接近到交互对象一定范围内时进行响应** It may be difficult for people to precisely touch specific points on objects that are small, thin, or placed at a distance. When your app detects a gesture near an interactive object, it's usually best to assume the user wants to affect the object.
+ **考虑用户发起的物品缩放是否必要** Scaling is generally appropriate when an object, like a toy or game character, doesn't have an intrinsic size and the user may want to see it larger or smaller. For an object with a finite size relative to the real world, like a piece of furniture, scaling is irrelevant if the item is placed at an accurate size. Scaling is not a remedy for adjusting the distance of an object—making an object larger to make it appear closer, for example, just results in a larger object that's still far away.
+ **警惕潜在的冲突手势** A two-finger pinch gesture, for example, is quite similar to a two-finger rotation gesture. If you implement two similar gestures like this, be sure to test your app and make sure they're interpreted properly.
+ **保证虚拟物品移动流畅** Objects shouldn't appear to jump when the user resizes them, rotates them, or moves them to a new location.
+ **探索更多吸引人的交互** Gestures aren't the only way for people to interact with virtual objects in AR. Your app can use other factors, like motion and proximity, to bring content to life. A game character, for example, could turn its head to look at the user as they walk toward it.

### 解决问题
+ **当交互不理想时允许用户重置** Don't force people to wait for conditions to improve or struggle with object placement. Give them a way to start over again and see if they have better results.
<div class="ARKit">
    <img src="https://developer.apple.com/ios/human-interface-guidelines/images/ARKit_01.svg" width = "40%"/>
    <img src="https://developer.apple.com/ios/human-interface-guidelines/images/ARKit_02.svg" width = "40%"/>
</div>

+ **问题出现时提出修复建议** Analysis of the user's environment and surface detection can fail for a variety of reasons—there's not enough light, a surface is too reflective, a surface doesn't have enough detail, or there's too much camera motion. If your app is notified of insufficient detail or too much motion, or if surface detection takes too long, offer suggestions for resolving the problem.

|            Problem             |              Possible suggestion              |
| ------------------------------ | --------------------------------------------- |
| Insufficient features detected | Try turning on more lights and moving around. |
| Excessive motion detected | Try moving your phone slower. |
| Surface detection takes too long | Try moving around, turning on more lights, and making sure your phone is pointed at a sufficiently textured surface. |

+ **只在硬件使用的设备上提供AR特性** If your app's primary purpose is AR, make your app available only to devices that support ARKit. If your app offers AR as a secondary feature—like a furniture catalog that includes product photos and allows some products to be viewed in AR—avoid displaying an error if the user tries to enter AR on an unsupported device. If the device doesn't support ARKit, don't present optional AR features in the first place. For developer guidance, see the arkit key in the [UIRequiredDeviceCapabilities](UIRequiredDeviceCapabilities) section of [Information Property List Key Reference](https://developer.apple.com/library/content/documentation/General/Reference/InfoPlistKeyReference/), and the [isSupported](https://developer.apple.com/documentation/arkit/arconfiguration/2923553-issupported) property of [ARConfiguration](https://developer.apple.com/documentation/arkit/arconfiguration).

### AR 符号
Apps can display an AR glyph in controls that launch ARKit-based experiences. You can download this glyph in [Resources](https://developer.apple.com/design/resources/#ios-apps).
<div class="ARKit">
    <img src="https://developer.apple.com/ios/human-interface-guidelines/images/ARKit_Glyph.svg" width = "40%"/>
    <img src="https://developer.apple.com/ios/human-interface-guidelines/images/ARKit_Glyph_Button.svg" width = "40%"/>
</div>

+ **不要滥用 AR 符号** The glyph should be used strictly for initiating an ARKit-based experience. Never alter the glyph (other than adjusting its size and color), use it for other purposes, or use it in conjunction with AR experiences not created using ARKit.
+ **保留所需最小的图标空间** The minimum amount of clear space required around an AR glyph is 10% of the glyph's height. Other elements shouldn't infringe on this space and occlude the glyph in any way.
![ARKit_Glyph_Clear](https://developer.apple.com/ios/human-interface-guidelines/images/ARKit_Glyph_Clear.svg)

### AR 徽章
包含多种类产品的应用可以使用徽章来表明能够使用AR观看的详细的项目。For example, a department store app might allow people to preview the appearance of select furniture products in their home before making a purchase.
![](https://developer.apple.com/ios/human-interface-guidelines/images/ARKit_Badging.svg)
+ **不要滥用 AR 徽章** You can download AR badges in [Resources](https://developer.apple.com/design/resources/#ios-apps). These images, which are available in collapsed and expanded forms, should be used strictly for the purpose of identifying products or other objects that can be viewed in AR using ARKit. Never alter the badges, change their color, use them for other purposes, or use them in conjunction with AR experiences not created using ARKit.
<table>
<tr style="width:100%;border-style: none;margin: 1px;padding: 1px">
<td style="width:45%;border-style: none;"><div>
      <img src="https://developer.apple.com/ios/human-interface-guidelines/images/ARKit_Badge_IconAndText.svg" />
      <p style = "text-align:center">AR badge</p>
    </div></td>
<td style="width:45%;border-style: none;"> <div>
      <img src="https://developer.apple.com/ios/human-interface-guidelines/images/ARKit_Badge_Icon.svg" />
      <p style = "text-align:center">Glyph-only AR badge</p>
    </div></td>
</tr>
</table>

The AR badge is preferable. In general, the glyph-only badge should be used when space is constrained and won't accommodate the AR badge. Both badges work well at their default size.

+ **只有在应用中同时包含可以用 AR 观看和不能用 AR 观看的物品时才使用 AR 徽章** If all objects in your app can be viewed in AR, then badging is redundant and unnecessary.
+ **保持徽章放置位置一致且清晰** A badge looks best when displayed in one corner of an object's photo. Always place it in the same corner and make sure it's large enough to be seen clearly (but not so large that it occludes important detail in the photo).
+ **保留所需最小的图标空间** The minimum amount of clear space required around an AR badge is 10% of the badge's height. Other elements shouldn't infringe on this space and occlude the badge in any way.

<div class="ARKit">
    <img src="https://developer.apple.com/ios/human-interface-guidelines/images/ARKit_Badge_IconAndText_Clear.svg" width = "40%"/>
    <img src="https://developer.apple.com/ios/human-interface-guidelines/images/ARKit_Badge_Icon_Clear.svg" width = "40%"/>
</div>

### 获悉更多
For developer guidance, see [ARKit](https://developer.apple.com/documentation/arkit).
