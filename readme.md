# MarkRight Blender

The idea here is to use MarkRight to control Blender and include the various steps as screenshots in between the
control blocks.

I good thing to display would be some Nodevember tutorials, e.g.: https://www.youtube.com/watch?v=sO0ulv7wz-0.

Not sure how to handle the Blender control yet, it's always possible to just build up a Python file and run it
through Blender, e.g.: https://github.com/TomasHubelbauer/blender-script

It might be possible to interface with Blender more directly, but not sure it is worth it, it comes down to how
painful nodes are to use through the Blender `bpy` Python interface.

The thing could look something like this (rough sketch):

~~~
```py cookie.py!
# Add sphere
# Add some nodes
# Take screenshot of this step
```

![](screenshot-1.png)

```py !
# Add more nodes
# Connect up existing nodes
# Tweak node values
# Take screenshot of this step
```

![](screenshot-2.png)
~~~

Et cetera.

Need to solve the exact syntax of the nodes. Also to avoid image metadata from marking the screenshots as
changed in Git, they should be compared as bitmaps against the existing first and only written if they
differ on the bitmap level.
