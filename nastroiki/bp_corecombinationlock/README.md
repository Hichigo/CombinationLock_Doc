# BP\_CoreCombinationLock

This blueprint implements the main logic of the lock, configures the control and functions of starting control and ending control of the lock.

An event (**OnCorrectPasswordEntered\_Disp**) has also been created, which is called after entering the correct password, to which you can subscribe from the outside (for example, to open a door or any other action).

To enter the correct password, you need to turn the knob in the desired direction to the correct number, example for 3 combinations:

1. Left to number 3
2. Right to number 8
3. Right to number 14

If the rotation goes in the wrong direction in which the lock expects, everything will be reset to the first combination.

## Settings

### Lock rotation

| **Variable name**  | **Type** | **Description**                                                                                   |
| ------------------ | -------- | ------------------------------------------------------------------------------------------------- |
| **TimerLoops**     | integer  | The number of rotation steps, affects the smoothness of the animation of the rotation of the lock |
| **RotateDuration** | float    | Rotation time to next digit                                                                       |

### Password

| **Variable name**             | **Type**    | **Description**                                                  |
| ----------------------------- | ----------- | ---------------------------------------------------------------- |
| **AmountPasswordCombination** | integer     | The number of combinations that must be entered to open the lock |
| **PasswordCombination**       | S\_Password | A data structure that specifies a password combination           |

### UI

| **Variable name** | **Type**   | **Description**     |
| ----------------- | ---------- | ------------------- |
| **UIClass**       | UserWidget | Control tips widget |

### Lock

| **Variable name**        | **Type** | **Description**                                                                                                  |
| ------------------------ | -------- | ---------------------------------------------------------------------------------------------------------------- |
| **NumberOfDigitsInLock** | integer  | Number of digits in the lock                                                                                     |
| **BigStepDigitRotation** | integer  | The number of digits that switches in one rotation works when the **shift** or **RT** (gamepad) key is held down |

### Camera

| **Variable name**     | **Type** | **Description**                     |
| --------------------- | -------- | ----------------------------------- |
| **TargetArmLength**   | float    | Distance from camera to lock        |
| **SprintArmRotation** | Rotator  | Rotating the camera around the lock |

### Sound

| **Variable name**         | **Type**  | **Description**                                                                  |
| ------------------------- | --------- | -------------------------------------------------------------------------------- |
| **CorrectPasswordSound**  | SoundBase | Sound when correct password is entered                                           |
| **RotateLockHandSound**   | SoundBase | The sound of the rotation of the handle of the lock                              |
| **WrongCombinationSound** | SoundBase | Sound when incorrect password combination is entered                             |
| **CorrectDigitSound**     | SoundBase | when rotated to the correct number, a sound will be emitted, as if hacked by ear |
