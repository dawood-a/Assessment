# Assessment

Kickstarter Tech UI Assessment



MAIN MENU Project



This Unity project demonstrates how to build a simple styled UI menu using the built-in Unity UI (UGUI) system. It features animated UI elements, hover effects, responsive layout, and mobile-friendly design including support for phone screen camera notches.



--------------------------------------------------------

PROJECT STRUCTURE:



Assets/

\- UI/

 	- Animations/		--> Contains idle and HandPointer animation clips.

 	- Images/		--> Includes self-made images for the background, buttons, HandPointer, and title.

 	- Scenes/		--> Contains the MainMenu scene file.

 	- Scripts/		--> C# scripts:

 					- "ButtonHover" Controls button hover effects and HandPointer behavior.

 					- "SafeArea" Manages the safe area layout, especially around mobile device notches.



--------------------------------------------------------

FEATURES AND EXPLANATION:



1\. BUTTONS:

 	- Includes three buttons: Play, Settings, and Quit.

 	- Each button is built using Unity's UI Button element.

 	- Buttons are grouped using a Vertical Layout Group for spacing and alignment.



2\. HOVER EFFECT:

 	- Each button has a child Image called "Highlight". This image uses a sprite with a colored border (like Gold) and is hidden by default.

 	- When the user hovers over a button (mouse or touch), a C# script "ButtonHover" enables the border image.

 	- A separate "HandPointer" image moves next to the hovered button to simulate a pointer.

 	- You can animate the HandPointer for a more dynamic interaction, or disable the animation by unchecking the animation checkbox.



3\. HAND POINTER MOVEMENT:

 	- The HandPointer is a single Image object placed under the Canvas.

 	- When hovering a button, it is repositioned next to the button.

 	- The script "ButtonHover.cs" handles activation and positioning of the hand.



4\. TITLE ANIMATION:

 	- "UNITY UI" is the main title displayed on the main menu screen.

 	- The top text element "INTRO TO" has a floating idle animation.

 	- This is done using Unity's Animator with a looping position animation to simulate bobbing or floating. The animation can be disabled by unchecking the animation chechbox.



5\. SAFE AREA SUPPORT:

 	- The "SafeArea.cs" script adjusts UI panels to stay within the screen’s safe area (avoiding notches and round corners).

 	- Attach this script to any UI container (e.g., top panel or entire layout container).



6\. RESPONSIVE UI:

 	- The Canvas Scaler is configured to scale UI based on screen size.

 	- UI Scale Mode: Scale With Screen Size

 	- Reference Resolution: 1920 x 1080

 	- Match Width Or Height: 0.259

 	- This allows UI to adapt to both portrait and landscape mode.



---------------------------------------------------------

HOW TO SET UP:



1\. Open the project in Unity.

2\. Open the scene from Assets/Scenes/SampleScene.unity.

3\. Add your custom sprite assets to Assets/Images/.

 	- Example: Main Menu background, Button backgrounds, border sprite, hand pointer image.

4\. Assign these sprites to the respective UI components.

5\. For each button, assign the "highlight" and "hand" references in the Inspector.

 	- Highlight: the border image child.

 	- Hand: the shared hand pointer object.



--------------------------------------------------------

RECOMMENDED IMAGE SETTINGS:



\- Set all UI images' Texture Type to: Sprite (2D and UI)

\- Use Image Type: "Sliced" (for scalable UI borders), or "Filled" for the texture to stretch across the entire element.



--------------------------------------------------------

TO ADD MORE BUTTONS:



1\. Duplicate one of the existing buttons in the ButtonContainer.

2\. Change its label or sprite.

3\. Assign new highlight border if needed.

4\. Reconnect references in the ButtonHover.cs script.



--------------------------------------------------------



