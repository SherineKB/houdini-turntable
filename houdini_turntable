### OBJECT PATH ###
node = hou.node("/obj/Turntable")
object = node.parm("object")

geo_path = object.eval()
geo_object = hou.node(geo_path)

### FRAMES NB ###
frames = node.parm("framesNumber")
frames_value = frames.eval()


### ROTATION ###

vex_expression = "fit(\$F, 1, {}, 0, 360)".format(frames_value)
    #the \ prevents Houdini from interpreting $F as a variable and treats it as a literal string within the expression.

## Axe Y
if not geo_object:
    print ("No object found")
else:

   geo_object.parm("ry").setExpression(vex_expression) 
