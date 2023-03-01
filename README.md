# Rotating brain in FIJI
This is a description of how to create a rotating brain in FIJI

### 1. Open the 3D image in FIJI
    Example image: Allen CCFv3 annotation map 25 um/voxel
   ![image](https://user-images.githubusercontent.com/60980561/222276762-45ce003c-75ab-4514-a1b8-849be88bc1fa.png)


### 2. Change the 3D image to RGB
    Method 1: Image > Color > Stack to RGB
  
    Method 2: Type > RGB Color
  
    (Skip this step may result of automatic contrast adjustment in later step)

  <img src="https://user-images.githubusercontent.com/60980561/222276241-3b1fd2b4-a7c9-46e4-b755-034b091bac01.png" width="400">
  

### 3. Open 3D Viewer
    Plugins > 3D Viewer
    
    Resolution is better when the Resampling factor = 1, but the computation time is longer. 
    Sometimes if the stacks is very big, Resampling factor = 1 may not work (program freezes)
    
   <img src="https://user-images.githubusercontent.com/60980561/222279626-8ba6a33d-a5ea-4ffe-8ab1-171d5568e3d3.png" width="400">
   
   With resampling factor = 1, it will give you the 3D version of the image as below
   <img src="https://user-images.githubusercontent.com/60980561/222280173-4a814515-35a6-4c10-b597-60c40620b270.png" width="700">
   

### 4. Record 360 deg rotation
    View > Record 360 deg rotation
   <img src="https://user-images.githubusercontent.com/60980561/222280684-c3877096-8a39-4da8-8860-838ad97d4d51.png" width="400">
    
    Once the recording started, you can see the brain is rotating. When it finished, the output is a timelapse movie
    
    Note: You can record a Movie with bigger view by simply maximizing the window to full screen before start recording.
   <img src="https://user-images.githubusercontent.com/60980561/222281055-50be54f4-8a5a-4dfd-81bc-4ddc1d615349.png" width="400">
   
   
   
   
### 5. Adjust the rotating speed
    Right click the 'play' button, you can see options for adjusting speed and other features
   <img src="https://user-images.githubusercontent.com/60980561/222282047-2b52db77-29a5-47d2-b7f5-63d929003409.png" width="400">
   
   
### 6. Export
    Method 1: to .gif: File > Save As > Gif...
      When there are too many colors, the color of gif may be off. You can try Method 2 described below.
      
    Method 2: to .avi: Plugins > Bio-Format > Bio-Format Exporter and export to .avi
              to .mp4: open the avi in Windows Video Editor > New Video Project > Add the avi to 'Project library' > drag it to the 'Storyboard' > Select 'Finish Video' and save it as mp4 file.
    

## Additional Notes
    1. When there are multiple channels, the images can be changed into Hyperstacks. You can adjust the LUT/Brightness/Contrast for individual channels. Once the adjustments are done, convert it to RGB.
    2. If you feel the movie is silight too dark or there something you want to adjust, you can use ImageJ function within a for loop in Macro. 
    Example for brightness adjustment:
        for (i = 1; i <=180; i++) {
            setSlice(i);
            setMinAndMax(0, 150);
        }
    

# Additional information
## Allen CCFv3 download    
    Link: http://help.brain-map.org/display/mouseconnectivity/API
    You can find the links here:
    
  <img src="(https://user-images.githubusercontent.com/60980561/222288010-359a6c09-18fb-4560-94b6-8a81d7d3bed4.png" width="400">
