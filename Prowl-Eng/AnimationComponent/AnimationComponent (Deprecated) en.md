# AnimationComponent (Deprecated)

> **Notice:** this component is deprecated. The notes below document the existing implementation.

## Selecting an animation

Playing a specific animation requires an `AssetRef` converted to the expected type. You can also retrieve an animation from the list stored in `AnimationComponent` with `GetInstance`; because this method returns an object, a cast is required.

![Getting an animation reference](../../Images/Pasted%20image%2020261007112935.png)

You can select a specific clip by its index.

![Selecting a clip by index](../../Images/Pasted%20image%2020261007113039.png)

![Additional animation selection example](../../Images/Pasted%20image%2020261007113936.png)

Another option is to use `RES` on the `AssetRef`.

![Using RES on the AssetRef](../../Images/Pasted%20image%2020261007114523.png)

These implementations rely on the animation list owned by the component.

## State machine with animations

When using a State Machine, compare the previous action with the current action, then update the previous value after the comparison. Because this runs every frame, failing to update the state can cause the animation to keep repeating.

![Comparing previous and current actions](../../Images/Pasted%20image%2020261011063213.png)

![Example of state update](../../Images/Pasted%20image%2020261011063031.png)

![Additional State Machine example](../../Images/Pasted%20image%2020261011063155.png)
