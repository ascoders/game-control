# game-control

game-control is a simple&fast game controller with pixi.js.

# How to use

```bash
npm i game-control
```

# Create root controller

```typescript
import { GameControl } from "game-control"

const preloadImages = ["/static/img1", "/static/img2"]
const gameControl = new GameControl(htmlElement, preloadImages, gameInit, gameLoop)

function gameInit(){}
function gameLoop(){}
```

# Create game object

```typescript
import { GameObject } from "game-control"

export default class Aircraft extends GameObject<PIXI.Sprite> {
    public onUpdate() {
        // game loop, you can move or do something..
    }
}
```

# Add and switch scene

```typescript
// add a new scene
gameControl.newScene("newScene")
// go to new scene
gameControl.goToScene("newScene")
```

# Add game object to scene

```typescript
gameControl.addGameObjectToScene(gameObject, "newScene")
// or default to current scene
gameControl.addGameObjectToScene(gameObject)
```