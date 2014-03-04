# Unity Made Awesome 0.1

This is a quick description on how to use UMA 0.1.

## Quick Action Hotkeys

### Reset Transform ###

**Alt+G - Reset Position**

This will set the local position of the object to (0, 0, 0).

**Alt+R - Reset Rotation**

This will set the local rotation of the object to (0, 0, 0).

**Alt+S - Reset Scale**

This will set the local scale of the object to (1, 1, 1).

### Others ###

Ctrl+Alt+N Create Empty Child

Creates an empty child to the selected object, the local position of this child is (0, 0, 0). If multiple objects are selected then the active object will become the parent. If no objects are selected then a GameObject is created at (0, 0, 0) with no parent.

## Transform Edit

You can now with the ease of hotkeys manipulate the transform of objects in the scene view. By selecting GameObject(s) in the scene window or hierarchy window, you can perform the following actions:

**G - Translate**

This will move the object parallel to the camera's view plane based off the motion of the mouse.

**T - Rotate**

This will rotate an object through an axis that is perpendicular to the camera's view plane. Considering the object's position as the center, the object will rotate based off of the angle of the mouse's original position and the current position of the mouse.

**S - Scale**

This will scale the object uniformly regardless of the viewing angle. Moving the mouse closer to the object's position will scale it down while moving away from the object will increase the scale.

Actions can be confirmed by pressing the hotkey that activated the transform again or by pressing enter. Actions can be canceled by pressing ESC or space.

### Single Axis Lock ###

While performing any transform action on an object. The action can be limited to a single axis by pressing the key for the axis desired to be locked. For example, to only rotate an object on the X axis then the key 'X' needs only be pressed while rotating an object. The same is true for the Y axis (key 'Y') and the Z axis (key 'Z').

The axis lock is in global space. To perform an axis lock in local space then press the desired axis key twice. For example, to translate an object forward (Z axis) then press 'Z' twice. The exception is for scaling an object. The scale action only performs in local space.

### Double Axis Lock ###

With any axis key press, if it is accompanied with shift then that axis is omitted from the axis lock allowing movement on the other two axis and restricting change on the selected axis. For example, if an object is already sitting on the ground and for it to remain on the flat ground by moved then by pressing Shift+Y then the object will move along its X and Z axis and there will be no change in the Y axis. Similar to single axis lock, the double axis lock first performs the lock in global space but by pressing the key combination again the lock will now be in local space.

### Increment Snapping ###

Any time while performing a transform edit, Ctrl may be pressed to toggle snapping. When snapping is enabled the object will snap to incremental values. For example, if enabled while translating then the object will snap to whole numbers when being moved, rotation snaps to 45 degree angles, and scale will snap to whole numbers.

### Configurable Options ###

In the UMA Configuration Window (UMA -> Configuration Window or Window -> UMA Configuration) there are options for altering the behavior of the transform editting.

**Snap By Default ** - If this is enabled then objects will snap by default when transform editing. When this is the case pressing Ctrl will toggle the non-snapping behavior.

**Translate Snap Increment** The increment from the global zero position to snap objects to. Default is 1.

**Rotate Snap Increment** The angle increment snap from zero rotation. Default is 45 degrees.

**Scale Snap Increment** The increment from no scaling (1, 1, 1) to snap the scaling to. Default is 1.

**'R' for Rotate** Use key 'R' instead of 'T' for rotation. Note, this will prevent the transform tool change in the scene view.

**Enable Mouse (iffy)** Enable the mouse to be used to confirm or cancel transforms. If enabled then left click will confirm a transform edit while right click will cancel an edit. However, there are limitations and issues to using this feature. The click must occur in the scene view and after a right mouse click, an additional click with the left click is necessary in order to select and object.

## Hiding Object(s)

In the sceneview, objects may be hidden so that they do not appear while working on the scene. These objects will be unhidden on play, when a scene is saved, or when scripts are compiled.

Object(s) can be hidden pressing 'H' when they are selected. This will turn off their renderers while they are considered hidden. Shift+H will hide all objects in the scene that are not currently selected. In order to manually unhide these objects, simply press Alt+H which will turn back on all renderers on objects hidden.

## Autosave

Now built in is an auto save for the scene currently being worked on. On scripting compilation, when playing, or after 5 minutes a saved copy of the scene will be stored in a umasaves folder that is created at the scene's location. Only one backup is maintained so this feature isn't really around to revert back to previous state but instead to prevent major loss of work if Unity crashes or your computer blows up but the harddrive managed to survive.