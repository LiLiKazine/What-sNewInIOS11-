What’s New in iOS 11

Learn about developing for iPhone X

-Super Retina Display | Human Interface Guidelines

Screen Size:
In portrait orientation, the width of the display on iPhone X matches the width of the 4.7" displays of iPhone 6, iPhone 7, and iPhone 8. The display on iPhone X, however, is 145pt taller than a 4.7" display, resulting in roughly 20% additional vertical space for content.
https://developer.apple.com/ios/human-interface-guidelines/images/OV_Screen_Size_47.svg
https://developer.apple.com/ios/human-interface-guidelines/images/OV_Screen_Size_iPhoneX.svg
Portrait dimensions	                Landscape dimensions
1125px × 2436px (375pt × 812pt @3x)	2436px × 1125px (812pt × 375pt @3x)

Supply high-resolution images for all artwork in your app. iPhone X has a high-resolution display with a scale factor of @3x. For glyphs and other flat, vector artwork, it's best to provide resolution-independent PDFs. For rasterized artwork, provide both @3x and @2x versions of your artwork. See Image Size and Resolution(https://developer.apple.com/ios/human-interface-guidelines/icons-and-images/image-size-and-resolution/) and Custom Icons(https://developer.apple.com/ios/human-interface-guidelines/icons-and-images/custom-icons/).

Layout:
When designing for iPhone X, you must ensure that layouts fill the screen and aren't obscured by the device's rounded corners, sensor housing, or the indicator for accessing the Home screen.
https://developer.apple.com/ios/human-interface-guidelines/images/OV_Fullscreen.svg
https://developer.apple.com/ios/human-interface-guidelines/images/OV_Clipping.png
Most apps that use standard, system-provided UI elements like navigation bars, tables, and collections automatically adapt to the device's new form factor. Background materials extend to the edges of the display and UI elements are appropriately inset and positioned.
https://developer.apple.com/ios/human-interface-guidelines/images/OV_UI_Appearance_47.png
https://developer.apple.com/ios/human-interface-guidelines/images/OV_UI_Appearance_X.png
For apps with custom layouts, supporting iPhone X should also be relatively easy, especially if your app uses Auto Layout and adheres to safe area and margin layout guides.

Preview your app on iPhone X. You can use Simulator (included with Xcode) to preview your app and check for clipping and other layout issues. Some features, like wide color imagery, are best previewed on actual devices.

Provide a full-screen experience. Make sure backgrounds extend to the edges of the display, and that vertically scrollable layouts, like tables and collections, continue all the way to the bottom.
https://developer.apple.com/ios/human-interface-guidelines/images/OV_LayoutGuides_Portrait.svg
https://developer.apple.com/ios/human-interface-guidelines/images/OV_LayoutGuides_Landscape.svg
Inset essential content to prevent clipping. In general, content should be centered and symmetrically inset so it looks great in any orientation and isn't clipped by corners or the device's sensor housing, or obscured by the indicator for accessing the Home screen. For best results, use standard, system-provided interface elements and Auto Layout to construct your interface. All apps should adhere to the safe area and layout margins defined by UIKit, which ensure appropriate insetting based on the device and context. The safe area also prevents content from underlapping the status bar, navigation bar, toolbar, and tab bar.

Be mindful of the status bar height. The status bar is taller on iPhone X than on other iPhones. If your app assumes a fixed status bar height for positioning content below the status bar, you must update your app to dynamically position content based on the user's device. Note that the status bar on iPhone X doesn't change height when background tasks like voice recording and location tracking are active.

If your app currently hides the status bar, reconsider that decision on iPhone X. The display height on iPhone provides more vertical space for content than the displays of 4.7" iPhones, and the status bar occupies an area of the screen your app probably won't fully utilize. The status bar also displays information people find useful. It should only be hidden in exchange for added value.
https://developer.apple.com/ios/human-interface-guidelines/images/OV_47_Display.svg
https://developer.apple.com/ios/human-interface-guidelines/images/OV_47_Cropped.svg
https://developer.apple.com/ios/human-interface-guidelines/images/OV_47_LetterBox.svg
https://developer.apple.com/ios/human-interface-guidelines/images/OV_iPhoneX_Display.svg
https://developer.apple.com/ios/human-interface-guidelines/images/OV_iPhoneX_Cropped.svg
https://developer.apple.com/ios/human-interface-guidelines/images/OV_iPhoneX_PillarBox.svg
Be mindful of aspect ratio differences when reusing existing artwork. iPhone X has a different aspect ratio than 4.7" iPhones. As a result, full-screen 4.7" iPhone artwork appears cropped or letterboxed when displayed full-screen on iPhone X. Likewise, full-screen iPhone X artwork appears cropped or pillarboxed when displayed full-screen on a 4.7" iPhone. Make sure that important visual content remains in view on both display sizes.

Avoid explicitly placing interactive controls at the very bottom of the screen and in corners. People use swipe gestures at the bottom edge of the display to access the Home screen and app switcher, and these gestures may cancel custom gestures you implement in this area. The far corners of the screen can be difficult areas for people to reach comfortably.

Don't mask or call special attention to key display features. Don't attempt to hide the device's rounded corners, sensor housing, or indicator for accessing the Home screen by placing black bars at the top and bottom of the screen. Don't use visual adornments like brackets, bezels, shapes, or instructional text to call special attention to these areas either.

Allow auto-hiding of the indicator for accessing the Home screen sparingly. When auto-hiding is enabled, the indicator fades out if the user hasn't touched the screen for a few seconds. It reappears when the user touches the screen again. This behavior should be enabled only for passive viewing experiences like playing videos or photo slideshows.

See Adaptivity and Layout(https://developer.apple.com/ios/human-interface-guidelines/visual-design/adaptivity-and-layout/).

Color:
The display on iPhone X supports a P3 color space, which can produce richer, more saturated colors than sRGB.

Use wide color to enhance the visual experience. Photos and videos that use wide color are more lifelike, and visual data and status indicators that use wide color are more impactful. See Color Management(https://developer.apple.com/ios/human-interface-guidelines/visual-design/color/#color-management).
https://developer.apple.com/ios/human-interface-guidelines/images/colorGraphic_wideColor.svg

Gestures:
The display on iPhone X uses screen-edge gestures to provide access to Home screen, app switcher, Notification Center, and Control Center.

Avoid interfering with systemwide screen-edge gestures. People rely on these gestures to work in every app. In rare cases, immersive apps like games might require custom screen-edge gestures that take priority over the system's gestures—the first swipe invokes the app-specific gesture and a second-swipe invokes the system gesture. This behavior (known as edge protect) should be implemented sparingly, as it makes it harder for people to access the system-level actions. See Gestures(https://developer.apple.com/ios/human-interface-guidelines/user-interaction/gestures/).

Additional Design Considerations:
Reference authentication methods accurately. iPhone X supports Face ID for authentication. If your app integrates with Apple Pay or other system authentication features, don't reference Touch ID on iPhone X. Likewise, make sure your app doesn't refer to Face ID on devices that support Touch ID. See Authentication(https://developer.apple.com/ios/human-interface-guidelines/user-interaction/authentication/).

Don't duplicate system-provided keyboard features. On iPhone X, the Emoji/Globe button and Dictation button automatically appear beneath the keyboard—even when using custom keyboards. Your app can't affect these buttons, so avoid causing confusion by repeating them in your keyboard. See Custom Keyboards(https://developer.apple.com/ios/human-interface-guidelines/extensions/custom-keyboards/).

Resources:
Download iPhone X UI design templates for Photoshop and Sketch in Resources(https://developer.apple.com/design/resources/#ios-apps).
