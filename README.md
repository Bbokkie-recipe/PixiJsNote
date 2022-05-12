# PixiJsNote
for pixiJs practice repository
https://user-images.githubusercontent.com/93479286/167424058-8818fe75-2d51-43cd-aff8-cd9f380bfbeb.mp4   
```
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />

    <title>Document</title>
    <style>
      body {
        margin: 0;
      }
      canvas {
        display: block;
        background-color: blue;
      }
    </style>
  </head>
  <body>
    <canvas id="mycanvas"></canvas>
    <script src="pixi.js"></script>
    <script type="text/javascript">
      const canvas = document.getElementById("mycanvas");
      // Create the application helper and add its render target to the page
      const app = new PIXI.Application({
        view: canvas,
        width: window.innerWidth,
        height: window.innerHeight,
      });

      // Create the sprite and add it to the stage
      const texture = PIXI.Texture.from("bike.png");
      const img = new PIXI.Sprite(texture);
      img.x = app.renderer.width / 2;
      img.y = app.renderer.height / 2;
      img.anchor.x = 0.5;
      img.anchor.y = 0.5;
      app.stage.addChild(img);

      app.ticker.add(animate);
      function animate() {
        img.rotation += 0.1;
      }
    </script>
  </body>
</html>

```
