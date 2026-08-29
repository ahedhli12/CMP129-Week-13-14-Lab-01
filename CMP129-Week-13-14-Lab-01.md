CMP 129 – Computer Science II
Weeks 13 and 14 – Lab 1: JavaFX Shapes, Effects, and Media
Learning Objectives

After completing this lab, students should be able to:

Create and display JavaFX shapes.
Apply colors and gradients to graphical objects.
Use visual effects such as Glow and DropShadow.
Enable and disable effects using event handlers.
Resize a shape using a Slider.
Play an audio or video file using JavaFX media classes.
Create Play, Pause, and Stop controls.
Organize interface components using layout panes.
Assignment Overview

Create a JavaFX application that displays multiple shapes, applies visual effects, and plays an audio or video file.

The application must include:

At least three different shapes.
Unique colors or gradients.
Two different visual effects.
Buttons to toggle the effects.
A slider that resizes one shape.
A media player with Play, Pause, and Stop buttons.
An organized layout using JavaFX layout panes.
Required Class

Create:

ShapesMediaApp.java

The class must extend Application:

public class ShapesMediaApp extends Application

Include the following method:

@Override
public void start(Stage primaryStage)

Also include a main() method:

public static void main(String[] args) {
    launch(args);
}
Part 1: Create the Shapes

Add at least three different JavaFX shapes. For example:

Circle
Rectangle
Polygon

Other JavaFX shapes may be used with the instructor’s approval.

Example declarations:

Circle circle = new Circle(60);
Rectangle rectangle = new Rectangle(140, 80);
Polygon triangle = new Polygon(
        0.0, 100.0,
        50.0, 0.0,
        100.0, 100.0
);

Each shape must:

Be clearly visible.
Have a different size or appearance.
Use a unique solid color or gradient.
Be displayed neatly inside the application window.
Part 2: Colors and Gradients

Use a different fill for each shape.

At least one shape must use a gradient, such as:

LinearGradient
RadialGradient

Example solid fills:

circle.setFill(Color.CORNFLOWERBLUE);
rectangle.setFill(Color.ORANGE);

Students should not use the same fill color for every shape.

Part 3: Visual Effects

Apply two different JavaFX effects. Recommended effects include:

Glow
DropShadow

Example:

Glow glow = new Glow(0.8);
DropShadow shadow = new DropShadow();

Apply the effects to different shapes. For example:

circle.setEffect(glow);
rectangle.setEffect(shadow);
Part 4: Toggle Effect Buttons

Add buttons that allow the user to turn each effect on and off.

Required buttons:

Toggle Glow
Toggle Shadow

Each button must:

Use an event handler.
Determine whether the effect is currently enabled.
Disable it if it is on.
Enable it if it is off.

The program may use Boolean variables to store the state:

private boolean glowEnabled = true;
private boolean shadowEnabled = true;

The buttons should work repeatedly, not only once.

Part 5: Shape-Resizing Slider

Add a Slider that changes the size of one shape.

For example, the slider may control the radius of the circle:

Slider sizeSlider = new Slider(20, 120, 60);
circle.radiusProperty().bind(sizeSlider.valueProperty());

The slider must include:

An appropriate minimum value.
An appropriate maximum value.
A reasonable starting value.
A label explaining what it controls.

Example label:

Circle Size

The shape should resize immediately as the user moves the slider.

Part 6: Media Player

Add an audio or video file to the project.

Students may use a supported format such as:

.mp3
.mp4
.wav
.m4a

Media compatibility may depend on the computer and JavaFX installation. An .mp3 audio file is recommended.

Create the media components using:

Media media = new Media(mediaFile.toURI().toString());
MediaPlayer mediaPlayer = new MediaPlayer(media);

If using video, also create:

MediaView mediaView = new MediaView(mediaPlayer);

Do not use a media URL that requires an Internet connection. The media file must be stored with the project and submitted.

Part 7: Media Controls

Create these three buttons:

Play
Pause
Stop

Implement the following behavior:

Play: Starts or resumes the media.
Pause: Temporarily pauses the media.
Stop: Stops the media and returns it to the beginning.

Example event handlers:

playButton.setOnAction(event -> mediaPlayer.play());
pauseButton.setOnAction(event -> mediaPlayer.pause());
stopButton.setOnAction(event -> mediaPlayer.stop());

All three controls must function correctly.

Part 8: Application Layout

Use JavaFX layout panes to arrange the elements neatly.

Recommended layout:

VBox for the main application layout.
HBox for the three shapes.
HBox for the effect buttons.
HBox for the media-control buttons.

A possible arrangement is:

------------------------------------------------
| JavaFX Shapes, Effects, and Media             |
|                                               |
|     Circle      Rectangle      Polygon        |
|                                               |
| Toggle Glow     Toggle Shadow                 |
|                                               |
| Circle Size: [---------- slider ----------]   |
|                                               |
|              Media Area                       |
|                                               |
|          Play      Pause      Stop            |
------------------------------------------------

Include appropriate:

Padding
Spacing
Alignment
Labels
Button sizes
Window dimensions
Functional Requirements

The completed application must allow the user to:

View at least three different shapes.
Identify a unique color or gradient on every shape.
See two different visual effects.
Toggle the first effect on and off.
Toggle the second effect on and off.
Resize one shape using a slider.
Play the selected media.
Pause the media.
Stop the media.
Continue using the controls without restarting the application.
General Requirements
Use JavaFX rather than Swing or JOptionPane.
Include at least three different JavaFX shapes.
Use unique colors or gradients.
Include at least one gradient.
Apply two different JavaFX visual effects.
Include working buttons that toggle both effects.
Include a slider that resizes one shape.
Include Play, Pause, and Stop buttons.
Store the media file within the project.
Use VBox, HBox, or another suitable layout pane.
Use meaningful variable and method names.
Include comments explaining the effects, media controls, and event handlers.
Display a descriptive application title.
Ensure that the application compiles and runs without errors.
Follow the course AI-use policy.
Record any AI assistance in AI-Use-Report.md.
Required Organization

Keep these files directly in the repository root:

- `CMP129-Week-13-14-Lab-01.md`
- `AI-Use-Report.md`
- `ShapesMediaApp.java`
- `media/` containing the media file used by the application

Do not create or use a `src` folder.


Replace sample.mp3 with the actual name of the media file used.

The Java file may begin with:

/*
 * Student Name:
 * Course: CMP 129
 * Week: 13
 * Lab: 1
 * Assignment: JavaFX Shapes, Effects, and Media
 * Date:
 */
Submission

Students must submit or push:

ShapesMediaApp.java
Lab-01/media/sample.mp3
Lab-01/AI-Use-Report.md

If a different media filename or format is used, submit that file instead.

Suggested commit messages:

Create JavaFX shapes and layout
Add visual effects and interactive controls
Add media player controls
Complete Week 13 JavaFX lab
