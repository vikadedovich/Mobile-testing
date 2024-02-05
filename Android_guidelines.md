# Basic guidelines:
## 1. System font - Roboto

## 2. Units

Density independent pixels (dp) and scalable pixels (sp) are essential for building layouts and presenting fonts that respond uniformly to the wide range of screen densities, size classes, form factors, and aspect ratios that make up Android devices.

__To calculate dp:__

`dp = (width in pixels * 160) / screen density`

## 3. Screen resolution (most popular)

`360 px x 640 px`

## 4. Shadows in the interface

Applied from 0 to 24 dp, shadows give elements a sense of volume. In "Material Design," material serves as a metaphor. The design is inspired by the real world, considering textures, surfaces, reflections from light, and object shadows. "Material" reimagines the concept of paper and inks.

## 5. Navigation

__More about Navigation:__

1. _System Bars_
   
Includes the status and navigation bars, show important info like battery level and time. They allow direct interaction from anywhere on the device. Keep them at the top of layers in app designs. Make them transparent or match the app's color.
The Android status bar has notification and system icons. Users can access the notification shade by pulling down the status bar. It can look different based on context, time, user preferences, and themes. You can set the status bar style, including the background color, transparency, and opacity, as part of your app's theme.

3. _Navigation bar_
   
On Android, users navigate using back, home, and overview controls. "Back" goes to the previous view, "Home" takes you to the device's home screen, and "Overview" displays open and recently used apps. Users can pick navigation bar styles, like gesture navigation (recommended) or three-button navigation.

__Bottom Navigation:__

_Navigation bar:_
   - Back returns directly back to the previous view.
   - Home transitions out of the app and to the device's home screen.
   - Overview shows the apps are open and have recently been opened. Users can choose from various navigation bar configurations including gesture navigation (recommended) and three-button navigation.
     
_Top-level Navigation:_
   - Bottom Navigation Bar Tabs
     
_Additional navigation:_
   - "Hamburger" button opens side menu "Navigation Drawer"
     
_Top Navigation:_
   - Top App Bar Title is aligned to the left, located near "hamburger" menu or near "back" button. It is not changed in size while scrolling the screen.

3. _Gesture Navigation_
   
Introduced in Android 10 (API level 29), gesture navigation is the recommended way to navigate, though you can't change the user's preference. It doesn't use buttons for back, home, and overview; instead, there's a single gesture handle. Users swipe from the screen edges to go back or forward, swipe up from the bottom to go home, and swipe up and hold to open the overview.

Gesture navigation works well on both mobile and larger screens. To ensure a good user experience:
   - Support edge-to-edge content.
   - Avoid placing interactions or touch targets under gesture navigation areas.
     
## 6. Search
   - To cancel search you need to tap "Back" button.
   - Search can be an icon. Icon can be opened in Top App Bar.
   - When search is essential component it is displayed firstly.
## 7. CTA button
Button is usually located in the bottom right corner.

## 8. Colors
  - For better accessibility:
  - Check color contrast and avoid similar tones.
  - Be mindful of red and green, which may be hard for color-blind users.
  - Use colors meaningfully; too many can be confusing or overwhelming.
  - Stick to a consistent color scheme; repeat patterns.
  - Build light and dark color schemes for different contexts.
  - Use color tokens to show the element's color role, avoiding hardcoded values.
  - Limit dynamic and static color sources in the same view.
  - Avoid mixing too many colors from different content pieces.
  - UI colors include accent, semantic, and surface colors.
  - Accent colors are core Android brand colors.
  - Semantic colors have specific meanings in Material 3.

## 9. Themes
A theme is a set of styles like color, type, and shape that can change how a user's mobile or large-screen device and in-app experience look and feel.

**Types of themes**
Themes are system-based or app-based. System themes affect the device UI, while app themes impact only the specific app. Your app must use one type, but app themes only affect the app itself. Some system theme settings can be changed in-app.

  - **System themes**:
    
System themes apply to the whole Android device, affecting individual apps based on user settings. They include light and dark themes, user-generated themes, and manufacturer themes.

__Light and Dark Themes:__
  1. Light theme (Day mode) has a bright display with higher luminance.
  2. Dark theme (Night mode) reduces luminance for better screen legibility in various conditions.
    
__User-generated Themes:__
User-generated themes use dynamic colors from a user's wallpaper, available with Material You starting in Android 12. This color palette generates light and dark color schemes.

__Manufacturer Themes:__
Device manufacturers may offer proprietary theming options affecting system UI and display settings.

  - **App themes**:
    
__Baseline:__
The Material library provides a baseline theme with a purple color scheme and Roboto font. Apps without defined theme attributes use these baseline attributes.

__Custom (Brand):__
Custom themes offer more expression for your app's look and feel, acting as a fallback when specific system themes aren't available. You can have multiple custom schemes for user selection, content inspiration, or sub-branded elements.

## 10. Layout
A layout sets up how a user interacts with your app visually, like in an activity. Android offers libraries and techniques for displaying and positioning content.

__Tips:__
  - Keep important interactions in an easily reachable screen area.
  - Group related content for a user-friendly flow.
  - Align similar content and UI elements consistently.
  - Parts of an Android App Screen:

__System Bars:__
The status and navigation bars (system bars) show vital info and allow device interaction. They're a crucial part of the interface. Add them as a top layer in designs to ensure proper layout and styling.

__Navigation Region:__
Navigation includes elements for app navigation and actions across Android.

__Body Region:__
The body region contains screen content. It should extend under navigation and system bars.

## 11. Grids
__Baseline Grid__
Using a grid ensures consistent spacing and alignment in your UI. Android's UI follows an 8 dp grid for layout, components, and spacing.

__Column Grid__
Columns create a vertical structure in the layout, dividing content within the body area. Align content with the grid for consistency but allow flexibility in sizing.

__Size Classes__
Window size classes are predefined breakpoints for responsive and adaptive layouts. Android has three classes: Compact, Medium, and Expanded.

__Aspect Ratios__
Aspect ratio is the width-to-height proportion of an element. Maintain consistency by using these recommended ratios across your UI:
   16:9, 
    3:2,
    4:3,
    1:1,
    3:4,
    2:3.

## 12. Immersive Content
Immersive mode hides system bars for a full-screen experience, ideal for video, games, images, and books to prevent accidental exits.

__Tips:__
   - Users can display UI by tapping the screen during video playback.
   - Don't permanently hide system bars on personal devices; designs should consider them for the best experience.
   - Use overlays for text and controls.
   - Combine immersive mode with features like picture-in-picture and Chromecast.
   - Use immersive mode when it significantly enhances the user experience, as it limits easy access to system navigation.
   - Fullscreen is suitable for content like games or uninterrupted video viewing but not always appropriate. Consider the user's need for an uninterrupted view or avoiding accidental exits.

## 13. Picture-in-picture (PiP)
is a type of multi-window mode intended for activities that play full-screen video. It lets the user watch a video in a small window pinned to a corner of the screen while navigating between apps or browsing content on the main screen.

## 14. Components
__Action Components:__
Help users achieve goals. Material offers various buttons, from FABs for primary actions to icon buttons for selecting options.

__Communication Components:__
Provide information through badges, progress indicators, and snackbars. Keep users informed about status and processes.

__Containment Components:__
Hold information and actions. Components like cards, dialogs, and tooltips group related content and actions visually. Lists can have explicit or implicit containment.

__Navigation Components:__
Aid navigation through the UI. Mobile uses navigation bars or drawers for primary destinations. Tabs, bottom app bars, and top app bars offer ways to navigate supporting information and actions.

__Selection Components:__
Let users make choices. Whether checkboxes in forms, chips for filtering, or switches for toggling settings, these components allow user input and control.

__Text Input Components:__
Enable text entry and editing. Text fields allow users to input text into the UI.

## 15. Split screen mode
Working with two applications at a time on divided screen.

## 16. User authentication with Passkeys
Passkeys are a safer and more convenient alternative to passwords, allowing users to sign in using biometrics, PIN, or pattern. This offers a seamless experience, eliminating the need to remember usernames or passwords.

__Tips:__
  - Introduce passkeys at the right moment to encourage user adoption.
  - Make passkeys the default option for a simple and secure sign-in.
  - Keep passkey information consistent across the product for user understanding.
  - Utilize the passkey icon for a consistent login experience.
  - Implement passkeys in your app using the Credential Manager API.
  - Use the Credential Manager API to streamline sign-in options without listing them all upfront.
  - Allow users to create a passkey after initial sign-in with a password or other methods.
    
## 17. Notifications
Notifications offer quick, timely, and relevant info about your app when not in use.
__Steps for implementing notifications:__
  - Learn about notification anatomy.
  - Pick the right notification type.
  - Set the notification category matching your chosen type.
