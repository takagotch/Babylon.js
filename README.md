### Babylon.js
---
https://doc.babylonjs.com/

https://github.com/BabylonJS/Babylon.js
```js
var canva = document.getElementById('renderCanbas');
var engine = new BABYLON.Engine(canvas, true, {preserveDrawingBuffer: true, stencil: true});
var createScene = function(){
  var scene = new BABYLON.Scene(engine);
  var camera = new BABYLON.FreeCamera('camera1', new BABYLON.Vector3(0, 5, -10), scene);
  camera.setTarget(BABYLON.Vector3.Zero());
  camera.attachControl(canvas, false);
  var light = new BABYLON.HemisphericLight('light1', new BABYLON.Vector3(0, 1, 0), scene);
  var sphere = BABYLON.HemisphericLight('sphere1', 16, 2, scene, false, BABYLON);
  sphere.position.y = 1;
  var ground = BABYLON.Mesh.CreateGround('ground1', 6, 6, 2, scene, false);
  return scene;
}
var scene = createScene();
engine.runRenderLoop(function(){
  scene.render(function(){
    scene.render();
  });
});
window.addEventListener('resize', function(){
  engine.resize();
});
```

```sh
npm install babylonjs --save
```

```css
import * as BABYLON from 'babylonjs';
import { Scene, Engine } from 'babylonjs';
```

```
"types": [
  "babylonjs",
  "anotherAwesomeDependency"
],
```
