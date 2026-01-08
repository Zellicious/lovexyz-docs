# engine.lua

The script that returns when you require lovexyz. <br>
Used to handle the main drawing, transforming, and shading processes. <br>

All meshes are rendered from [```triangles.lua```](triangles.md).


## **Parameters**


### ```engine.canvas ``` 

The main canvas when drawing to the window.
<br>
<br>

### ```engine.depthCanvas``` 

The depth buffer of the main canvas.
<br>
<br>


### ```engine.graphicsScale ```

The main canvas resolution multiplier based on screen resolution.
<br>
<br>


----

### ```engine.lighting``` 

A container consisting of lighting parameters to be used by the renderer.
<br>
<br>

#### ```engine.lighting.solidSkyColor``` 

The default sky color if skybox is not rendered.
<br>
<br>

#### ```engine.lighting.sunDirection``` 

The sun direction.
<br>
*note: sun direction will be normalized in the shader*
<br>
*note: direction is pointing from world origin to sun direction*
<br>
<br>

#### ```engine.lighting.ambient``` 

The ambient value to be used in ```engine.transformShader``` .
<br>
<br>

#### ```engine.lighting.specShininess``` 

The specular exponent to be used in ```engine.transformShader``` .
<br>
<br>

#### ```engine.lighting.specStrength``` 

The specular strength to be used in ```engine.transformShader``` .
<br>
<br>

#### ```engine.lighting.shadowEnabled``` 

Boolean to check for shadows, updating ```engine.shadowMap```, and used in ```engine.transformShader``` .
<br>
<br>

#### ```engine.lighting.simpleShadows``` 

Boolean to toggle PCF or direct sampling for shadows, used in ```engine.transformShader``` .
<br>
<br>

#### ```engine.lighting.specularEnabled``` 

Boolean to check for speculars to be used in ```engine.transformShader``` .
<br>
<br>

#### ```engine.lighting.diffuseEnabled``` 

Boolean to check for diffuse to be used in ```engine.transformShader``` .
<br>
<br>

#### ```engine.lighting.skyboxEnabled``` 

Boolean to draw the skybox.
<br>
<br>

----

### ```engine.lighting.colorCorrection``` 

Color correction values to be used in ```engine.colorCorrection```
<br>
<br>

#### ```engine.lighting.colorCorrection.brightness``` 

Brightness of the screen (default = 1).
<br>
<br>

#### ```engine.lighting.colorCorrection.contrast``` 

Contrast of the screen (default = 1).
<br>
<br>

#### ```engine.lighting.colorCorrection.saturation``` 

Saturation of the screen (default = 1).
<br>
<br>


----

### ```engine.cam``` 

A container consisting of camera information.
<br>
<br>

#### ```engine.cam.pos``` 

A ```vec3``` of the camera position in world space.
<br>
<br>

#### ```engine.cam.rot``` 

A ```vec3``` of the camera rotation in euler angles.
<br>
<br>

#### ```engine.cam.fov``` 

Field of view of the camera in radians.
<br>
<br>

#### ```engine.cam.matrix``` 

Camera offset matrix.
<br>
*note: real camera matrix is handled internally*
<br>
<br>

----

### ```engine.skyboxShader``` 

The skybox shader used when rendering to the main canvas if ```engine.lighting.skyboxEnabled``` is true.
<br>
<br>


### ```engine.transformShader``` 

The main shader used when rendering to the main canvas, handles projection and lighting based on ```engine.lighting``` params.
<br>
<br>

### ```engine.colorCorrection``` 

The color correction shader.
<br>
<br>

### ```engine.transformOnly``` 

Shader used for custom depth canvases.
<br>
<br>

### ```engine.proj``` 

Perspective projection of the main camera.
<br>
<br>

### ```engine.skyboxFormat```

Vertex format of the skybox.
<br>
<br>

### ```engine.skyboxMesh``` 

Mesh of the skybox.
<br>
<br>

### ```engine.skyTexture``` 

The texture of the skybox.
<br>
*note: call ```engine.skyboxMesh:setTexture(engine.skyTexture)``` everytime you make changes to the sky texture*
<br>
<br>

### ```engine.shadowMap``` 

A canvas containing orthographic depth information from the sun's view.
<br>
<br>

### ```engine.shadowSize``` 

A number to be used by ```engine.sunProj```.
<br>
<br>

### ```engine.sunProj``` 

Orthographic projection matrix of the sun.
<br>
<br>

## **Functions**


### ```engine.perfDebug()``` 

Debug panel showing average fps and live fps.
<br>
<br>

### ```engine.draw()``` 

Handles and draws everything needed for the rendering.
<br>
<br>

### ```engine.refreshCanvases()``` 

Refresh canvases that are altered by resolution.
<br>
<br>