# triangles.lua

The script that is used to parse and store model meshes. <br>
Uses [```obj.lua```](obj.md) to parse obj files and convert them to mesh data <br>

Default global: ```triangles``` <br>

## Parameters


### ```triangles.meshes```

Stores loaded meshes.
<br>
<br>


### ```triangles.loadedModels```

Stores loaded models.
<br>
<br>


### ```triangles.textureCache```

Stores cached textures.
<br>
<br>


### ```triangles.format```

The vertex format when creating a new triangle/model.
<br>
<br>


## Functions




----

### ```triangles.loadModel(path,usage,lookupName)```

Loads a model and returns a model (table) class.
<br>
<br>

#### ```model```

The returned model class when calling ```triangles.loadModel()```.
<br>
<br>

#### ```model.mesh```

The model mesh that is stored in ```triangles.meshes```.
<br>
<br>

#### ```model.transformMatrix```

The models ```mat4``` to alter the vertexes of the model when rendering.
<br>
<br>

#### ```model.visible```

Toggles the models visibility when rendering.
<br>
<br>

----