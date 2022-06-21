### EX NO:02
### DATE:13.04.2022
# <p align="center"> Roll a Ball</p> 

## Aim:
To Roll a Ball using C# program in unity .

## Algorithm:
### Step1: 
To Create a unity project in unity hub.

### Step 2: 
Aftern creating Click File -> Scene -> Select the scene -> Save as-> New folder(Scenes)-> File name (Expno2).

### Step 3: 
Click Hierarchy -> 3DObject -> Sphere Hierarchy -> 3DObject -> plane Hierarchy.

### Step 4: 
Create a folder in project and name as Materials Material folder -> Create -> Material (Name: Sphere) Inspector ->Surface Inputs ->BaseMAp (Choose the color) Drag the Cylinder to the plane and release the mouse

Create a folder in project and name as Materials Material folder -> Create -> Material (Name: Plane) Inspector ->Surface Inputs ->BaseMAp (Choose the color) Drag the Capsule to the plane and release the mouse

### Step 5: 
Create a folder name Coding and create a C# file to add the coding in it.

### Step 6: 
To add our C# Script file to our selected object, click on the C# Script file and drag it to Sphere objects in the Hierarchy window and run the application.

### Step 7: 
After run the application, you press the WASD and space key the ball will move and jump.

### Step 8: 
Save the unity file and take screenshot.

### Step 9: 
Close the Unity project.

## Program:
```c#
using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class NewBehaviourScript : MonoBehaviour
{

    public float xForce = 1.0f;
    public float yForce = 1.0f;
    public float zForce = 200.0f;   // Start is called before the first frame update
    void Start()
    {
        
    }

    // Update is called once per frame
    void Update()
    {
        float x = 0.0f;
        if(Input.GetKey(KeyCode.A))
        {
            x = x - xForce;
        }
        if (Input.GetKey(KeyCode.D))
        {
            x = x + xForce;
        }
        float z = 0.0f;
        if(Input.GetKey(KeyCode.S))
        {
            z = z - zForce;
        }
        if(Input.GetKey(KeyCode.W))
        {
            z = z + zForce;
        }
        float y = 0.0f;
        if(Input.GetKeyDown(KeyCode.Space))
        {
            y = yForce;
        }
        GetComponent<Rigidbody>().AddForce(x, y, z);
    }
}
```
## Output:

![ar2](https://user-images.githubusercontent.com/75235402/166145307-45900ed6-c1e4-4979-b23b-e9b825c34efa.jpg)


## Result:
Thus, The 3D application for Roll the Ball objects in unity is developed successfully.
