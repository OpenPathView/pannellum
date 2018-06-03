# API Events

## `load`

Fired when a panorama finishes loading.


## `scenechange`

Fired when a scene change is initiated. A `load` event will be fired when the
new scene finishes loading. Passes scene ID string to handler.


## `scenechangefadedone`

If a scene transition fade interval is specified, this event is fired when the
fading is completed after changing scenes.


## `error`

Fired when an error occured. The error message string is passed to the
event listener.


## `errorcleared`

Fired when an error is cleared.


## `mousedown`

Fired when the mouse button is pressed. Passes `MouseEvent` to handler.


## `mouseup`

Fired when the mouse button is released. Passes `MouseEvent` to handler.


## `touchstart`

Fired when a touch starts. Passes `TouchEvent` to handler.


## `touchend`

Fired when a touch ends. Passes `TouchEvent` to handler.

## Panorama view events

| Event              | Data                    | Description   |
| ------------------ | ----------------------  | ------------- |
| movestart          | [ViewEvent](#ViewEvent) | Fired when the user start moving in the panorama (start dragging, look animation ...). |
| move               | [ViewEvent](#ViewEvent) | Fired repeatedly as the user moves in the panorama. |
| moveend            | [ViewEvent](#ViewEvent) | Fired when the user stop moving in the panorama (stop dragging, look animation ended). |

# Event objects

## ViewEvent

Data about the view when the event was triggered. Exemple of event data view object  :
```javascript
{
    "hfov": 94.569177,
    "pitch": 20.2789,
    "yaw": 0.25436,
}
```

| Property          | Type      | Description                             |
| ----------------- | --------- | --------------------------------------- |
| hfov              | _number_  | Horizontal field of view in degrees     |
| pitch             | _number_  | Pitch orientation in degrees            |
| yaw               | _number_  | Yaw orientation in degrees              |