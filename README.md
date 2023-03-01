# Rotating brain in FIJI
This is a description of how to create a rotating brain in FIJI

### 1. Open the 3D image in FIJI
    Example image: Allen CCFv3 annotation map 25 um/voxel
   ![image](https://user-images.githubusercontent.com/60980561/222276762-45ce003c-75ab-4514-a1b8-849be88bc1fa.png)


### 2. Change the 3D image to RGB
    Method 1: Image > Color > Stack to RGB
  
    Method 2: Type > RGB Color
  
    (Skip this step may result of automatic contrast adjustment in later step)
  
  ![image](https://user-images.githubusercontent.com/60980561/222276241-3b1fd2b4-a7c9-46e4-b755-034b091bac01.png)

### 3. Open 3D Viewer
    Plugins > 3D Viewer
    
    Resolution is better when the Resampling factor = 1, but the computation time is longer. Sometimes if the stacks is very big, Resampling factor = 1 may not work (program freezes)
    
   ![image](https://user-images.githubusercontent.com/60980561/222278059-df9c875c-0a5e-44e1-93a5-99260a419b55.png)

 
