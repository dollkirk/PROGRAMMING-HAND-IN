#LEARNING JOURNAL

###TASK ONE-TURRET

PROBLEM:
I did not know how to get the turret object to rotate in the direction of the player. I knew it was to do with transform, however, I did not know what rotation function was needed.

SOLUTION:
I decided to go onto Unity Docs and search rotate. I had a scroll of all the rotate functions until I came across transform.LookAt: https://docs.unity3d.com/2021.3/Documentation/ScriptReference/Transform.LookAt.html
I then followed the instructions to create the turret movement




PROBLEM:
When the player moved around the turret, the barrel of the turret was facing the wrong direction. The barrel need to be facing towards the player as this would be wear the bullets would appear from.


SOLUTION:
I opened the turret prefab and rotated the cylinder barrel round to the opposite side of the capsule body.












PROBLEM:
I knew that I had to use Instatiate to create the bullets, however, I also needed the bullets to move at a high velocity in a forward-facing direction. I did not know how to do this.

SOLUTION:
I opened up Unity Docs again and searched up Instantiate: https://docs.unity3d.com/2021.3/Documentation/ScriptReference/Object.Instantiate.html
There were many examples on this page with instantiating projectiles so this helped a lot.

PROBLEM:
I applied one of the examples (the Rigidbody example) to the projectile script, however, It caused the bullets to constantly spawn every frame due to the Instantiate function happening in the update method.

SOLUTION:
I created an if statement and 2 float variables to check the fire rate and the time since the last fire. This would only instantiate a bullet after an interval of time.
































###TASK TWO- AREA COUNTDOWN

PROBLEM:
I had created a countdown timer by using TMPro and made it subtract by using time.deltaTime when it was more than 0. However, I did not know how to convert the float variable of the countdown to a string. 

SOLUTION:
I found a website that showed how to display the float as a string and also only display certain units in the number: https://gamedevbeginner.com/how-to-make-countdown-timer-in-unity-minutes-seconds/#convert_to_text 
I also asked my peer if there was an easier way to round the seconds and they showed me the use of string.Format("{0:n0}",timeCountDown)




PROBLEM:
I created a cube, deleted its mesh, set the trigger on the box collider on and named it CountResetCollider. I then created an 'OnTriggerEnter' method to reset the timeCountDown float back to 60. The timer was not resetting when the player entered the cube collider.

SOLUTION:
The timer script was attached to the UI canvas from back when I was trying to make the timer work. I moved the script over to the player cube so that the ‘OnTriggerEnter’ method knew what needed to trigger the collider.


###TASK THREE- ENLARGE PLAYER PICKUP 

PROBLEM:
I created a pickup script so that when the player collides with the pickup object, the pickup disappears. When tested, the pickup would fall from the sky like desired, however, when it would collide with the plane, the plane collider triggered the collision and destroyed the pickup. 

SOLUTION:
I assigned the player object to the tag “Player” and used an if statement to compare tag and then destroyed when it is “Player”.


PROBLEM:
I created an if statement in the pickup script in the update function to countdown from 5 seconds. When the timer hit 0, it would shrink the player back to 1 in all axis, to its original size. However, this did not work as when the player would collide with the pickup, the pickup would destroy, therefore the pickup script would not countdown as it was attached to the pickup.

SOLUTION:
I asked a peer to help, and they showed me how to reference a script in another script. I used this to create a separate timer script and attached it to an empty game object called controller. This also meant moving the transforms for increasing and decreasing the player’s size to this script.

