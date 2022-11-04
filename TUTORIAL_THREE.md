# TUTORIALS
## WEEK 3-ENLARGE PLAYER PICKUP

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


#### 

