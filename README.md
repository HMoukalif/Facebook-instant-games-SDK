**Learn how to integrate games built with JavaScript and HTML5 with Facebook instant games SDK**

**1. You need to start creating your game client. The game client needs to have an index.html file in the root directory. Start by importing the Instant Games SDK by adding this line in the head of your game before the </ head> Tag.**

```
<script src="https://connect.facebook.net/en_US/fbinstant.6.2.js"></script>
```


**2. Start loading game assets by adding this Script in the body of your game after the < body> Tag.**

```

<script>
  FBInstant.initializeAsync().then(function() {
    FBInstant.setLoadingProgress(100);
  });
  FBInstant.startGameAsync().then(function() {
    game.start();
  })
</script>
```


**3. You need to create a new file named fbapp-config.json and place the following code in it**
```

{
  "instant_games": {
    "orientation": "PORTRAIT", 
    "navigation_menu_version": "NAV_FLOATING"
  }
}
```

**The fbapp-config.json file should be saved in the main folder of the game (the same folder that contains index.html)**

**You can now compress the whole folder in zip format and upload it to Facebook.**
