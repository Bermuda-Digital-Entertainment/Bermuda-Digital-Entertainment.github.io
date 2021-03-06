---
layout: default
---
# York Pirates!
## About This Website
This is the website for the York Pirates! game.
This game is made by Bermuda Digital Entertainment (Team 7) for an Engineering 1 group project at the University of York, based off work by Bass2 (Team 14).

[The game can be downloaded from our GitHub repository](https://github.com/Bermuda-Digital-Entertainment/York-Pirates-2/releases/tag/1.0.1).

- [**Home**]() - This page will go over what York Pirates! is, how to play it, and provide information about how our code works.
- [**GitHub**](https://github.com/Bermuda-Digital-Entertainment/York-Pirates-2) - Our GitHub repository contains all the code for the project, as well as downloads.
- [**Assessment 1**](/assessment1) - Work by Bass2 for the first half of the project.
    - [**Deliverables**](assessment1/deliverables) - All the project deliverables will be listed here.
    - [**Plan**](/assessment1/plan) - Information about how the project was planned throughout development is shown here.
    - [**Use Case**](/assessment1/usecase) - Shows our planned use case for the game.
    - [**Files**](/assessment1/files) - Any additional files are listed here.
- [**Assessment 2**](/assessment2) - Work by Bermuda Digital Entertainment for the second half of the project.
    - [**Deliverables**](assessment2/deliverables)
    - [**Plan**](/assessment2/plan)
    - [**Use Case**](/assessment2/usecase)
    - [**Files**](/assessment2/files)

![Game Logo](/media/Logo.gif)

## The Game
<hr/>
### Animated Title Screen
![Title Screen](/media/Title_Screen.gif)
<br/>
Application comes with a main screen, where you can enter a name of your choice, start the game, and view our wonderful title graphic!
<hr/>
### Dynamic Tutorial
![Tutorial](/media/Tutorial.gif)
<br/>
Our game begins with a tutorial to show even the least inventive player just how to get 100% out of York Pirates!
<hr/>
### Fluid Goal Indicators
![Indicators](/media/Indicators.gif)
<br/>
In addition to our seamless movement, the game contains indicators so that you're never lost in our wonderfully crafted map environment!
<hr/>
### Fast Paced Combat!
![Combat](/media/Combat.gif)
![Combat](/media/Combat2.gif)
<br/>
Engage in fierce and engaging combat against colleges that feature individually processed projectiles to keep you on your toes!
<hr/>
### Game Over...
![Game Over](/media/Game_Over.gif)
<br/>
No punches (or in this case cannonballs) were pulled during the making of this game, and player death is implemented and possible!
<hr/>
### Player Tasklist
![Tasks](/media/Tasks.gif)
<br/>
In addition to allowing inferior foes to join your ranks (complete with full image and palette swaps!), defeating colleges and other commendable tasks award you with well-earned loot!
<hr/>
### Game Win!
![Game Win](/media/Game_Win.gif)
<br/>
Once all the colleges are captured and you are as satisfied with the gameplay experience as you are with our code, return to your home college to win the game (and pick our code to win at life)!

<hr/>

## The Code

### Scene2D.UI

We use LibGDX Sprite2D's UI system to allow User Interface and Heads Up Display (HUD) to be easily rendered and customised.

```java
// Make a table
Table table = new Table();
table.setBackground(skin.getDrawable("Background"));

// Create widgets
Image title = new Image(titleTexture);
ImageButton button = new ImageButton(skin, styleName: "Restart");

// Add widgets to table
table.add(title).expand();
table.row();
table.add(button).expand();
```
But that's not all...

![Debug Mode](/media/Debug.gif)
Featuring a UI debug mode! All at the flip of a boolean.

<hr/>

### ScreenAdapter

To make managing the project easy, we use LibGDX's ScreenAdapter. 
This package allows many screens for both gameplay and menus to be easily put together and organised as their own classes.
The easiest way to get the best project structure!

```java
public class ScreenName extends ScreenAdapter {
    
    public ScreenName() {
        // Initialise the screen
    }
    
    @Override
    public void render(float delta) {
        // Called every frame
        // Perform calculations
        // Render graphics
    }
    
    @Override
    public void dispose() {
        // Dispose of assets when done to improve performance
    }
}
```

<hr/>

### TiledMap
Using LibGDX's package for Tiled maps is the easiest way to rapidly produce gameplay levels.
The software [Tiled](https://www.mapeditor.org) can be used to produce levels, with easy to use wide-ranging functionality, it's the industry's best for a reason!
<br/><br/>![Tiled](/media/tiled.gif)
<br/><br/>Maps from Tiled can be easily imported into LibGDX, and we've even implemented our own collision system around it - ready out of the box!

# [Check out](https://github.com/Bermuda-Digital-Entertainment/York-Pirates-2) our repository on GitHub!
