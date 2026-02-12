# BP\_CoreSafe

Basic blueprint of the safe, which implements:

* transfer of control to the lock, if the trace got into the safe
* door opening animation
* animation of rotation of the door handle before opening
* attaching the lock to the door

## Settings

| **Variable name** | **Type**                | **Description**   |
| ----------------- | ----------------------- | ----------------- |
| **LockRef**       | BP\_CoreCombinationLock | Reference to lock |
| **OpenDoorAngle** | float                   | Open door angle   |
