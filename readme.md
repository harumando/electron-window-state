This repository is a fork of [mawie81/electron-window-state](https://github.com/mawie81/electron-window-state)
It shares all the functionality the original repo has, but this version also can save window state to an already existing JSON file. To do that you need to pass `object_path` property to `windowStateKeeper` function

```js
  let mainWindowState = windowStateKeeper({
    defaultWidth: 1000,
    defaultHeight: 800,
    object_path: 'settings.window.position',
    path: 'app-settings.json'
  });
```
So your `app-settings.json` file would look like this

```
  {
    ...
    ...
    settings: {
      window: {
        position: { Here will be the window state }
      }
    }
  }
```
