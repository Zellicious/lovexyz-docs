# engine.lua

The script that returns when you require lovexyz. <br>
Used to handle the main drawing, transforming, and shading processes. <br>

## Parameters

The modifiable parameters for engine.lua

#### ```engine.canvas ``` 


The main canvas when drawing to the window.
<br>
<br>

#### ```engine.depthCanvas``` 

The depth buffer of the main canvas.
<br>
<br>


#### ```engine.graphicsScale ```

The main canvas resolution multiplier based on screen resolution.
<br>
<br>


#### ```engine.skyboxShader``` 

The skybox shader used when rendering to the main canvas if ```engine.lighting.skyboxEnabled``` is true.
<br>
<br>


#### ```engine.transformShader``` 

The main shader used when rendering to the main canvas, handles projection and lighting based on ```engine.lighting``` params.
<br>
<br>


## Functions
