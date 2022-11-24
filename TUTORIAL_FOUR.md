# TUTORIALS
## WEEK FOUR-PRESSURE PLATES

#### PLAYER CONTROLLER:

Create a player object and a plane.

Then, create a C# script called PlayerController and attach it to the player object.

In this PlayerController script, above the Start function, create a public float variable called speed. Creating this as public means that we can input and edit this value in the Unity editor.

In the Update function, create 2 local float variables called h and v. 

![Screenshot 2022-11-04 201036](https://user-images.githubusercontent.com/114989045/200065791-53ea03ba-88bf-4ca1-b717-a404b6985ffa.png)

As shown in the image above, these 2 variables are set as the inputs from the user. Input.GetAxis means that it needs 2 input values that are opposites. Horizontal gets the horizontal arrow keys (left and right) and vertical gets the vertical arrow keys (up and down).

Next, we need to use these input values and move the player object based on the float values. transform.Translate does this. By putting the variable h in the x co-ordinate and v in the z co-ordinate, this moves the player object in the direction of the floats inputted by the player.

This movement needs to have a speed so multiply these co-ordinates by the variable speed.

I have also put in a jump input shown below, however, you do not need this for this tutorial.

![Screenshot 2022-11-04 201102](https://user-images.githubusercontent.com/114989045/200065804-820af291-4bf4-46c4-be8b-e0d32bc192ef.png)

#### USING TRANSFORM:

Create 2 diferent coloured game objects and attach rigidbody components to both so that the player object can move them around. These will be the key objects that will be placed on the corresponding pressure plates.

Also create 2 thin game objects placed on the plane. These will be the pressure plates that will be interacted with to open doors. To not confuse things, set the colours of these pressure plates to match the colours of the key game objects.

Create 2 more gameobjects that will be the doors that open when the key object is placed ontop of the pressure plate object.

![Screenshot 2022-11-24 211543](https://user-images.githubusercontent.com/114989045/203864018-7cb6d907-68c5-4d89-b2f6-0b54d8722ed6.png)

Lastly, as shown in the image above, create duplicates of these doors, switch off the mesh and colliders for these objects, and name one "DoorOpenPos" and the other "DoorClosePos" for both doors. These will be the positions of the doors when opened and closed.

Now, create a C# script called "DoorController" and attach this script to both doors. In this script create a public bool variable called "openDoor" and set it to false as the door should not be open to start with. 

Create 2 more public variables which will be Transform variables. This means that the variable is using the transforms (position, rotation, etc.) of the selected game object. Name these 2 Transform variables "doorOpenPos" and "doorClosePos". 

In the Update function, create an if statement to check if "openDoor" is equal to true. If it is, then we are going to move the door that this script is attached to, to where the "doorOpenPos" object position is. We can do this by using transform.position as shown below.


![Screenshot 2022-11-24 214149](https://user-images.githubusercontent.com/114989045/203866472-e9430924-3bc8-48e6-b0f8-6ff71b720458.png)

We also have to create an if statement to say when the door is not open. This is essentially the same if statement as before, however, it is checking if "doorOpen" is equal to false and setting the position of the door to the same as "doorClosePos".

![Screenshot 2022-11-24 214550](https://user-images.githubusercontent.com/114989045/203866814-6fcedf6d-288a-4191-a92d-31d68ec41ca8.png)


#### USING RIGIDBODY:
