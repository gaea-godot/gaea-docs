# Anatomy of a Graph

Graphs in Gaea all have to lead to the Output Node in order for the generation to work. Let's take a look at what each element in the nodes mean:

## Slots

![A screenshot highlighting the input and output slots of nodes](/../assets/tutorials/anatomy-of-a-graph/slots.png)

Gaea nodes have input and output slots. They're located on the left and right sides of the nodes, respectively. Input slots for arguments (such as in the SimplexSmooth2D node, see `frequency`, `lacunarity` & `octaves`), allow for overriding the values set in the node interface, but are **optional**.

This is how you'll connect nodes to each other. Click and drag on a slot to create a wire, then connect that to another slot of the same type.

### Slot Types
Slot types are differentiated by their colors:

| Type | Color & Shape | Description | Example |
| --- | --- | --- | --- |
| Number | Gray Circle | Can be a `float` or an `int`. | ![FloatVariable node](/../assets/tutorials/anatomy-of-a-graph/float_example.png) |
| Material | Red Diamond | A `GaeaMaterial` resource. Learn more about it in [How Gaea Works](/how-gaea-works.md) | ![MaterialVariable node](/../assets/tutorials/anatomy-of-a-graph/material_example.png) |
| Data | White Square | A grid of floats. | ![SimplexSmooth2D node](/../assets/tutorials/anatomy-of-a-graph/data_example.png) |
| Map | Green Tag | A grid of `GaeaMaterial`s. | ![MergeMaps node](/../assets/tutorials/anatomy-of-a-graph/map_example.png) | 
| Range | Pink Ring | A range between one number and another | ![ComposeRange node](/../assets/tutorials/anatomy-of-a-graph/range_example.png) |
| Boolean | Yellow Rounded Square | `true` or `false` | ![BoolConstant node](/../assets/tutorials/anatomy-of-a-graph/bool_example.png) |
| Vector2/3 | Light Blue Triangle/Purple Hourglass | 2/3 numbers: `x`, `y` and `z` | ![Vector2Constant and Vector3Constant nodes](/../assets/tutorials/anatomy-of-a-graph/vector_examples.png) |


# Special Nodes

## Frame

![A frame holding 3 nodes, with the title "Create noise and map tiles to it"](/../assets/tutorials/anatomy-of-a-graph/frame.png)

Frames can be used to organize your graphs. You can attach nodes to them, and they'll automatically resize to fit them. Right click frames to get option dropdowns, such as: changing the title, changing the background color, etc.