# JM
**Jennifer Yu, Mansour Elsharawy**

_Period 5, APCS2 Brown Mykolyk_

*Fixed Bugs:*

(Severity is the measure of how devastating the bug would've been if gone unfixed. Goes from 1 (low severity) to 5 (very high severity).)

| Problem| Solution|Severity|
|-------------|-------------|:-----:|
| Screen did not show balls growing and shrinking.|Ditched the while loop, realized draw() is repeatedly invoked.|4|
| Compilation error stating a curly brace was missing.|Though the error highlighted code in the Ball class, the missing curly bracewas actually within the Driver class.|1|
| Mouse-click would affect balls that did not collide.|Mouse-click changed the global variable within the Driver class. Problem remedied by placing a state variable within the Ball class instead, so each ball would have to keep track of its own individual state.|4|
|Balls would grow, not reach their max size, and leave residue on the screen, never shrinking.|Once a collision has been made after a mouse click, a ball should not have to be colliding with another ball to grow and shrink. A collision should change the state of the ball, leading to a whole other process that is independent of future collisions.|3|
|Balls that were shrinking would just become very small balls, but still visible.|See solution directly above.|3|
|Balls that had radius 0 were technically still points, and other balls would collide into what would seem to be empty space, yet begin the process of expansion.|Balls that shrunk to radius 0 would be in state 3, and then would be removed from the overall ArrayList of remaining balls. This means that though the balls still exist as points, the other remaining balls would only interact with the balls in the ArrayList.|2|

*Unfixed Bugs*

|Problem|Possible solution|Severity|
|--|--|:-:|
