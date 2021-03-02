_**HScript & VEX Variables**_
===

## _**Errors Or Omissions**_
A lot of this is probably factually inaccurate, outdated or both. However I have found it difficult to get a one stop overview of natively available values in VEX so this is a starting point reference ...albeit one that should be viewed sceptically.

## _**Global Variables**_

> Mostly taken from the [SideFX docs](http://www.sidefx.com/docs/houdini/network/expressions.html)<br />
> The global variables are commonly, though not exclusively, used in expressions rather than wrangles.

_Geometry_<br />
**$BBX** Bounding box x.<br />
**$BBY** Bounding box y.<br />
**$BBZ** Bounding box z.<br />
**$SIZEX** Bounding box x length.<br />
**$SIZEY** Bounding box y length.<br />
**$SIZEZ** Bounding box z length.<br />
**$PT** Index of a point.<br />
**$CEX** Centroid x.<br />
**$CEY** Centroid y.<br />
**$CEZ** Centroid z.<br />
**$XMIN** Bounding box corner.<br />
**$YMIN** Bounding box corner.<br />
**$ZMIN** Bounding box corner.<br />
**$XMAX** Bounding box corner.<br />
**$YMAX** Bounding box corner.<br />
**$ZMAX** Bounding box corner.

_Particles_<br />
**$AGE** Number of seconds a particle has been alive.<br />
**$LIFE** $AGE normalised to between 0 & 1.

_Playback_<br />
**$FPS** Playback speed in frames per second (as set with the Playbar controls).<br />
**$FSTART** Frame number of the first frame of animation (as set with the Playbar controls).<br />
**$NFRAMES** (the number of frames in the animation) = $FEND - $FSTART + 1.<br />
**$FEND** Frame number of the last frame of animation (as set with the Playbar controls).<br />
**$F** The current frame.<br />
**$FF** Floating point frame number.<br />
**$NFRAMES** Number of frames in the animation. $NFRAMES = $FEND - $FSTART + 1.<br />
**$RFSTART** Frame number of the first frame shown in the playbar.<br />
**$RFEND** Frame number of the last frame shown in the playbar.<br />
**$T** Current time in seconds. Equals ($F-1)/$FPS<br />
**$TLENGTH** Total length of animation in seconds.<br />
**$TSTART** Start time of animation in seconds.<br />
**$TEND** End time of animation in seconds.<br />
**$ST** Float simulation time.<br />
**$SF** Float simulation frame.

_General_<br />
**$ACTIVETAKE** Contains the name of the current take.<br />
**$E** The mathematical constant e (2.71828…).<br />
**$HFS** The directory where Houdini is installed.<br />
**$HH** $HFS/houdini.<br />
**$HIP** The directory containing the current scene file.<br />
**$HIPFILE** The full path of the current scene file, including the file extension.<br />
**$HIPNAME** The name of the current scene file without the extension. You can use this to build filenames with different extensions based on the scene name.<br />
**$HOME** Your home directory.<br />
**$JOB** The project directory.<br />
**$PI** The mathematical constant pi (3.1415926…).<br />

_Channels_<br />
**$OS** Operator String. Contains the current OP’s name.<br />
**$CH** Current channel name.<br />
**$IV** In value (value at start of segment).<br />
**$OV** Out value.<br />
**$IM** In slope.<br />
**$OM** Out slope.<br />
**$IA** In acceleration.<br />
**$OA** Out acceleration.<br />
**$LT** Local time - not including stretch or offset.<br />
**$IT** Start time of segment.<br />
**$OT** End time of segment.<br />
**$LIT** Local start time of segment.<br />
**$LOT** Local end time of segment.<br />
**$PREV_IT** Previous segment start time.<br />
**$NEXT_OT** Next segment end time.<br />

_COPS_<br />
**$CSTART** Start frame of the current COP.<br />
**$CEND** End frame of the current COP.<br />
**$CFRAMES** Number of frames for the current COP.<br />
**$CFRAMES_IN** Number of frames available from the first input COP.<br />
**$CINC** Gets the global frame increment value.<br />
**$W** Current image width.<br />
**$H** Current image height.

_Render Nodes_<br />
**$N** Current frame being rendered.<br />
**$NRENDER** Number of frames being rendered.

## _**Local / Geometry attributes**_

**@age** Time a particle has been alive.<br />
**@nage** <br />
**@accel** <br/>
**@center** <br/>
**@dPdx** <br/>
**@dPdy** <br/>
**@dPdz** <br/>
**@scale** <br/>
**@force** <br/>
**@rest** <br/>
**@torque** <br/>
**@up** Up vector.<br/>
**@uv** <br/>
**@v** Velocity vector.<br/>
**@backtrack** <br />
**@orient** Rotation as a quarternion.<br />
**@rot** Additional rotation quarternion, applied after the orientation attribute.<br />
**@trans** For copies and instances, translation vector to apply.<br />
**@pivot** For copies and instances, the local pivot vector.<br />
**@shop_materialpath** <br />
**@material_override** <br />
**@pscale** Floating-point scale factor of a point.<br />
**@ptnum** The current point's index.<br />
**@numpt** Total number of points on the geometry.<br />
**@primnum** The current primitive's index.<br />
**@numprim** Total number of primitives (faces) on the geometry.<br />
**@vtxnum** Presumably the vertex index?<br />
**@numvtx** Total vertices?<br />
**@P** Position as a 3 column vector.<br />
**@P\.x** Position named index.<br />
**@P\.y** Position named index.<br />
**@P\.z** Position named index.<br />
**@Cd** Color as a 3 column array.<br />
**@Cd\.r** Color named index. Value is normalised between 0 & 1.<br />
**@Cd\.g** Color named index. Value is normalised between 0 & 1.<br />
**@Cd\.b** Color named index. Value is normalised between 0 & 1.<br />
**@N** Normals<br />
**@id** Unique identifier for the current point (@ptnum can be reassigned).<br />
**@ix** <br />
**@iy** <br />
**@iz** <br />
**@nextid** <br />
**@pstate** <br />
**@resx** <br />
**@resy** <br />
**@resz** <br />
**@group_\*** <br />
**@name** <br />
**@_volume_name_** In a volume wrangle, read or write to a volume.<br />
**@instance** <br />
**@Frame** Float frame ($T).<br />
**@Time** Float time ($FF).<br />
**@SimTime** Float simulation time ($ST), only present in DOP contexts.<br />
**@SimFrame** Float simulation frame ($SF), only present in DOP contexts.<br />
**@TimeInc** Float time step (1/$FPS).

## _**Intrinsics**_
**"typename"** <br />
**"measuredarea"** <br />
**"measuredvolume"** <br />
**"transform"** <br />
**"viewportlod"** <br />
**"bounds"** <br />
**"pivot"** <br />
**"unexpandedfilename"** <br />
**"abcframe"** <br />
**"abcobjectpath"** <br />
**"abcfilename"** <br />
**"abctypename"** <br />
**"activevoxelcount"** <br />
**"volumevisualmode"** <br />
**"vdb_value_type"** <br />
**"vdb_is_saved_as_half_float"** Disk space saver.

# VEX Wrangle Cheat Sheet
_**Found %amp; taken from John Kunz | August 22nd, 2018**_
===

**_Global Variables._**
A list of variables available in wrangles. The type indicator isn't needed, but is included as a reminder. Available in all SOP wrangles
```
f@Frame     //The current floating frame number, equivalent to the $FF Hscript variable
f@Time      //The current time in seconds, equivalent to the $T Hscript variable
i@SimFrame  //The integer simulation timestep number ($SF), only present in DOP contexts.
f@SimTime   //The simulation time in seconds ($ST), only present in DOP contexts.
f@TimeInc   //The timestep currently being used for simulation or playback.

// Available in Attribute Wrangle
v@P         //The position of the current element.
i@ptnum     //The point number attached to the currently processed element.
i@vtxnum    //The linear number of the currently processed vertex.
i@primnum   //The primitive number attached to the currently processed element.
i@elemnum   //The index number of the currently processed element.
i@numpt     //The total number of points in the geometry.
i@numvtx    //The number of vertices in the primitive of the currently processed element.
i@numprim   //The total number of primitives in the geometry.
i@numelem   //The total number of elements being processed.

// Available in Volume Wrangle
v@P                     //The position of the current voxel.
f@density               //The value of the density field at the current voxel location.
v@center                //The center of the current volume.
v@dPdx, v@dPdy, v@dPdz  //These vectors store the change in P that occurs in the x, y, and z voxel indices.
i@ix, i@iy, i@iz        //Voxel indices. For dense volumes (non-VDB) these range from 0 to resolution-1.
i@resx, i@resy, i@resz  //The resolution of the current volume.
```

_Common Geometry Attributes._<br />
Frequently used attributes. Houdini knows to cast these to the appropriate VEX datatype.

```
// Int
@id         // A unique number that remains the same throughout a simulation.

// Float
@pscale     // Particle radius size.  Uniform scale.  Set display particles as 'Discs' to visualize.
@width      // Thickness of curves.  Enable 'Shade Open Curves In Viewport' on the object node to visualize.
@Alpha      // Alpha transparency override.  The viewport uses this to set the alpha of OpenGL geometry.
@Pw         // Spline weight.

// Vector3
@P          // Point position.  Used this to lay out points in 3D space.
@Cd         // Diffuse color override.  The viewport uses this to color OpenGL geometry.
@N          // Surface or curve normal.  Houdini will compute the normal if this attribute does not exist.
@scale      // Vector scale.  Allows directional scaling or stretching (in one direction).
@rest       // Used by procedural patterns and textures to stick on deforming and animated surfaces.
@up         // Up vector.  The up direction for local space, typically (0, 1, 0).
@uv         // UV texture coordinates for this point/vertex.
@v          // Point velocity.  The direction and speed of movement in units per second.

// Vector4
@orient     // The local orientation of the point (represented as a quaternion).
@rot        // Additional rotation to be applied after orient, N, and up attributes.

// String
@name       // A unique name identifying which primitives belong to which piece.  Also used to label volumes.
@instance   // Path of an object node to be instanced at render time.
```

_Specifying VEX Data Types_<br />
The following characters are used to cast to the corresponding data type.
```
float       f@name    // Floating point scalar values.
vector2     u@name    // Two floating point values. Could be used to store 2D positions.
vector3     v@name    // Three floating point values. Usually positions, directions, normals, UVW or colors.
vector4     p@name    // Four floating point values. Usually rotation quaternions, or color and alpha (RGBA).
int         i@name    // Integer values (VEX uses 32 bit integers).
matrix2     2@name    // Four floating point values representing a 2D rotation matrix.
matrix3     3@name    // Nine floating point values representing a 3D rotation matrix or 2D transform matrix.
matrix      4@name    // Sixteen floating point values representing a 3D transform matrix.
string      s@name    // A string of characters.
```

_Channel Shortcut Syntax_<br />
This is the syntax used to hint at the data type of auto generated wrangle parameters.
```
ch('flt1');             // Float
chf('flt2');            // Float
chi('int');             // Integer
chv('vecparm');         // Vector 3
chp('quat');            // Vector 4 / Quaternion
ch3('m3');              // 3x3 Matrix
ch4('m4');              // 4x4 Matrix
chs('str');             // String
chramp('r', x);         // Spline Ramp
vector(chramp('c', x)); // RGB Ramp
```


_Accessing Attributes on Other Inputs and Nodes_<br />
This syntax is used to refer to nodes wired into the inputs of the wrangle, or other nodes in the network.
```
// 'opinput:X' is the most legible and always works (the first input is input 0).
point('opinput:0', 'P', i@ptnum)
point('opinput:1', 'P', i@ptnum)
point('opinput:2', 'P', i@ptnum)
point('opinput:3', 'P', i@ptnum)

// The integer input number (the first input is 0).  Some functions don't support this but it's easy to type.
point(0, 'P', i@ptnum)
point(1, 'P', i@ptnum)
point(2, 'P', i@ptnum)
point(3, 'P', i@ptnum)

// @OpInputX works as well, but be careful as it isn't 0 based, instead it starts at 1 which is confusing
point(@OpInput1, 'P', i@ptnum)
point(@OpInput2, 'P', i@ptnum)
point(@OpInput3, 'P', i@ptnum)
point(@OpInput4, 'P', i@ptnum)

// v@opinputX_* reads an attribute from the same element on the numbered input (first input is input 0).
v@opinput0_P
v@opinput1_P
v@opinput2_P
v@opinput3_P

// Absolute and relative paths to other nodes look like this.
point('op:/obj/geo1/OUT', 'P', i@ptnum)
point('op:../../OUT', 'P', i@ptnum)
```

_Copying and Instancing Attributes_<br />
When copying or instancing, Houdini looks for these point attributes to customize each copy/instance.
```
p@orient                    // Orientation of the copy.
f@pscale                    // Uniform scale.
v@scale                     // Non-uniform scale.
v@N                         // Normal (+Z axis of the copy, if no p@orient).
v@up                        // Up vector of the copy (+Y axis of the copy, if no p@orient).
v@v                         // Velocity of the copy (motion blur), used as +Z axis if no p@orient or v@N.
p@rot                       // Additional rotation (applied after the orientation attributes above).
v@P                         // Translation of the copy.
v@trans                     // Translation of the copy, in addition to v@P.
v@pivot                     // Local pivot point for the copy.
3@transform or 4@transform  // Transform matrix overriding everything except v@P, v@pivot, and v@trans.
s@shop_materialpath         // The instanced object uses this material.
s@material_override         // A serialized Python dictionary mapping material parameter names to values.
s@instance
s@instancefile              // File path indicating what geometry to instance.
s@instancepath              // Geometry to instance. This is either a path to a file on disk or an op: path.
```


_DOP Particle Attributes_<br />
A particle system is first and foremost driven by attributes. Here are some of the attributes used.
```
f@age       // Time in seconds since the particle was born.
f@life      // Time in seconds the particle is allowed to live. When f@age>f@life, i@dead will be set to 1.
f@nage      // Normalized age, f@age divided by f@life.  Implicit attribute, you cannot write to this.
i@dead      // Whether a particle is living (0) or dead (1).  A dead particle is deleted in the Reaping stage.
i@id        // A unique id for the particle that remains the same throughout a single simulation.

i@stopped   // Whether a particle is moving (0) or stopped (1).
i@stuck     // Whether a particle is free (0) or stuck (1).
i@sliding   // Whether a particle is free (0) or sliding along a surface (1).
f@cling     // Force applied to sliding paritcles inwards (according to the collision's surface normal).
s@pospath   // The path to the object that the particle is colliding with.
i@posprim   // Which collision primitive in the path geometry whose position we wish to refer to.
v@posuv     // Parametric uv on the collision primitive.

i@hittotal  // The cumulative total of all hits for the particle (only incremented once per timestep).
i@has_pprevious // This is set to 1 if v@pprevious contains valid values.
v@pprevious // Stores the position of the particle on the previous frame.  Used for collision detection.
i@hitnum    // The number of times the particle collided in the last POP Collision Detect.
s@hitpath   // The path to the object that was hit. A path to a file on disk or an op: path.
i@hitprim   // The primitive hit. Could be -1 if it the collision detector couldn’t figure out which prim.
v@hituv     // The parametric UV space on the primitive.
v@hitpos    // Where the hit actually occurred.  Useful if the colliding object was moving.
v@hitnml    // The normal of the surface at the time of the collision.
v@hitv      // The velocity of the surface at the time of the collision.
f@hittime   // When the collision occurred, that could be within a frame.
f@hitimpulse// Records how much of an impulse was needed for the collision resolution.  varies with timestep.
f@bounce    // When particles bounce off another object, this controls how much energy they keep.
f@bounceforward // Controls how much energy they keep in the tangential direction.
f@friction  // When particles bounce, they are slowed down proportional to how hard they hit.
s@collisionignore   // Objects that match this pattern will not be collided.

f@force     // Forces on the particle for this frame.
f@mass      // Inertia of the particle.
v@spinshape // This is multiplied by f@pscale to determine the shape of the particle for rotational inertia.
f@drag      // How much the particle is effected by any wind effects.
f@dragexp   // Ranges from 1 to 2, default is set on the solver.  Used for both angular and linear drag.
v@dragshape // How much the particle is dragged in each of its local axes.
v@dragcenter// If specified, drag forces will also generate torques on the particle.
v@targetv   // The local wind speed. Thought of as the goal, or target, velocity for the particle.
f@airresist // How important it is to match the wind speed.  Thickness of the air.
f@speedmin  // Minumum speed, in units per second, that a particle can move.
f@speedmax  // Maximum speed, in units per second, that a particle can move.

p@orient    // Orientation of the particle.  Used for figuring out 'local' forces.
v@w         // Angular speed of the particle.  A vector giving the rotation axis.
v@torque    // The equivalent of force for spins. No inertial tensor (the equivalent of mass) is supported.
v@targetw   // The goal spin direction and speed for this particle.
f@spinresist// How important it is to match the targetw.
f@spinmin   // Minumum speed in radians per second that a particle can spin.
f@spinmax   // Maximum speed in radians per second that a particle can spin.
```


_DOP Grains Attributes_<br />
Particles under control of POP Grains have the ispbd attribute set to 1. This causes them to not perform normal movement update in the POP Solver, as the actual motion update is done in this node.
```
i@ispbd     // A value of 1 causes the particle to behave as grains.
f@pscale    // Used to determine the radius of each particle.
f@repulsionweight   // How much the particle collision forces are weighted.
f@repulsionstiffness// How strongly particles are kept apart.  Higher values result in less bouncy repulsion.
f@attractionweight  // How much the particles will naturally stick together when close.
f@attractionstiffness   // How strongly nearby particles stick to each other.
v@targetP   // Particles are constrained to this location.
f@targetweight      // The weight of the v@targetP constraints.
f@targetstiffness   // The stiffness with which particles are fixed to their v@targetP attribute.

f@restlength// Particles connected by polylines will be forced to maintain this distance (prim attribute).
f@constraintweight  // Scale, on a per-particle basis of the constraint force.
f@constraintstiffness   // This controls the stiffness on a per-particle basis.
f@strain    // This primitive attribute records how much the constraint is stretched.
f@strength  // If f@strain exceeds this primitive attribute, the constraint will be removed.
```


_DOP Packed RBD Attributes_<br />
The Bullet Solver uses several point attributes to store the properties of each piece of a packed object.
```
i@active    // Specifies whether the object is able to react to other objects.
i@animated  // Specifies whether the transform should be updated from its SOP geometry at each timestep.
i@deforming // Specifies whether the collision shape should be rebuilt from its SOP geometry each timestep.

f@bounce    // The elasticity of the object.
i@bullet_add_impact // Impacts that occur during the sim will be recorded in the Impacts or Feedback data.
i@bullet_ignore     // Specifies whether the object should be completely ignored by the Bullet solver.
f@bullet_angular_sleep_threshold// The sleeping threshold for the object’s angular velocity.
f@bullet_linear_sleep_threshold // The sleeping threshold for the object’s linear velocity.
i@bullet_want_deactivate// Disables simulation of a non-moving object until the object moves again.
i@computecom// Specifies whether the center of mass should be computed from the collision shape.
i@computemass   // Specifies whether the mass should be computedfrom the collision shape and density.
f@creationtime  // Stores the simulation time at which the object was created.
i@dead  // Specifies whether the object should be deleted during the next solve.
f@density   // The mass of an object is its volume times its density.
f@friction  // The coefficient of friction of the object.
f@inertialtensorstiffness   // Rotational stiffness.  A scale factor applied to the inertial tensor.
i@inheritvelocity   // v and w point attributes from the SOP geometry will override the initial velocity.
f@mass  // The mass of the object.
s@name  // A unique name for the object. Used by Constraint Networks.
p@orient// The orientation of the object.
v@P     // The current position of the object’s center of mass.
v@pivot // The pivot that the orientation applies to. If i@computecom is non-zero, this is auto-computed.
v@v     // Linear velocity of the object.
v@w     // Angular velocity of the object, in radians per second.

i@bullet_adjust_geometry    // Shrinks the collision geometry.
i@bullet_autofit    // Use the bounds of the object for Box, Capsule, Cylinder, Sphere, or Plane.
f@bullet_collision_margin   // Padding distance between collision shapes.
s@bullet_georep     // Can be convexhull, concave, box, capsule, cylinder, compound, sphere, or plane.
i@bullet_groupconnected     // Create convex hull per set of connected primitives.
f@bullet_length     // The length of the Capsule or Cylinder collision shape in the Y direction.
v@bullet_primR  // Orientation of the Box, Capsule, Cylinder, or Plane collision shape.
v@bullet_primS  // Size of the Box collision shape.
v@bullet_primT  // Position of the Box, Sphere, Capsule, Cylinder, or Plane collision shape.
f@bullet_radius // Radius of the Sphere, Capsule, or Cylinder collision shape.
f@bullet_shrink_amount  // Specifies the amount of resizing done by Shrink Collision Geometry.

s@activationignore  // Won't be activated by collisions with any objects that match this pattern.
s@collisiongroup    // Specifies the name of a collision group that this object belongs to.
s@collisionignore   // The object will not collide against any objects that match this pattern.
f@min_activation_impulse// Minimum impulse that will cause the object to switch from inactive to active.

f@speedmin  // Minumum speed, in units per second, that a particle can move.
f@speedmax  // Maximum speed, in units per second, that a particle can move.
f@spinmin   // Minumum speed in radians per second that a particle can spin.
f@spinmax   // Maximum speed in radians per second that a particle can spin.
f@accelmax  // Limits the change in the object’s speed that is caused by enforcing constraints.
f@angaccelmax   // Limits the change in the object’s angular speed that is caused by enforcing constraints.

f@airresist // Specifies how important it is to match the target velocity (v@targetv).
f@drag      // How much the the v@targetv and f@airresist attributes effect the object.
f@dragexp   // Ranges from 1 to 2, default is set on the solver.  Used for both angular and linear drag.
v@force     // Specifies a force that will be applied to the center of mass of the object.
f@spinresist// Specifies how important it is to match the target angular velocity (v@targetw).
v@targetv   // Target velocity for the object. Used in combination with the f@airresist attribute.
v@targetw   // Target angular velocity for the object. Used in combination with the f@spinresist attribute.
v@torque    // Specifies a torque that will be applied to the object.

i@bullet_autofit_valid  // Stores whether the solver has already computed collision shape attributes.
i@bullet_sleeping   // Tracks whether the object has been put to sleep by the solver.
f@deactivation_time // Amount of time the speed has been below the Linear Threshold or Angular Threshold.
i@found_overlap // Used by the solver to determine whether it has performed the overlap test.
i@id    // A unique identifier for the object.
i@nextid// Stores the i@id the solver will assign to the next new object.
```


_DOP Constraint Network Attributes_<br />
You can create attributes on the geometry to customize each constraint’s behavior and type. If a primitive attribute with the same name as a constraint property (such as damping) is present, the attribute value will be multiplied with the value from the constraint sub-data.
```
i@anchor_id  // The anchor’s position will be bound to this point (or vertex).
i@anchor_type   // Specifies if the anchor is attached to a point, vertex or agent transform.
v@condir// The normal of a plane (i@condof==1) or axis (i@condof==2) the object can move on or rotate about.
i@condof// Identifies the number of constrained degrees of freedom for an anchor (0 to 3).
s@name  // The object the constraint is attached to.  An empty name attaches to world space position.
v@P     // Identifies the initial world space position of the anchor.
p@orient// Initial world space orientation of the anchor.  Takes precedence over v@r point attribute.
v@r     // Identifies the initial world space orientation of the anchor as Euler angles.
v@v     // Identifies the velocity of the world space position to which the constraint is attached.
v@w     // Identifies the angular velocity of the world space position to which the constraint is attached.

s@constraint_name   // Prim attribute specifying the Data Name of the constraint to create.
s@constraint_type   // Prim attribute specifying degrees of freedom ('position', 'rotation' or 'all').
s@next_constraint_name  // Prim attribute specifying the next constraint_name to use after broken.
s@next_constraint_type  // Prim attribute specifying the next constraint_type to use after broken.
i@propagate_iteration   // Detail attribute specifying number of impact propagations for glue constraints.

f@force     // Prim attribute updated by the solver to contain the force applied to satisfy the constraint.
f@distance  // Prim attribute updated by the solver to contain the distance between it's anchors.
f@torque    // Prim attribute updated by the solver to contain the torque applied to satisfy the constraint.
f@angle     // Prim attribute updated by the solver to contain the angle (in radians) between the anchors.
f@impact    // Prim attribute updated by the solver to contain the accumulated impulses for the glue bond.

i@group_broken  // Any constraints that are in the broken primitive group will be ignored by solvers.
```


_DOP Wire Attributes_<br />
You can create attributes on the wire object’s RestGeometry to influence its behavior. Most of these attributes allow fine-tuning of the wire by scaling values set in this node. Point, primitive, or detail attributes of the same name will be used if the vertex attributes are not present.
```
f@width  // Width of each edge.
f@density   //  Density of each point.
p@orient// Initial orientation of each point. This value is stored as a quaternion.
v@v     // Initial velocity of each point.
v@w     // Initial angular velocity of each point measured in radians per second.
f@friction  // Friction of each point.
f@klinear   // Defines how strongly the wire resists stretching.
f@damplinear// Defines how strongly the wire resists oscillation due to stretching forces.
f@kangular  // Defines how strongly the wire resists bending.
f@dampangular   // Defines how strongly the wire resists oscillation due to bending forces.
f@targetstiffness   // Defines how strongly the wire resists deforming from the animated position.
f@targetdamping // Defines how strongly the wire resists oscillation due to stretch forces.
f@normaldrag// The component of drag in the directions normal to the wire.
f@tangentdrag   // The component of drag in the direction tangent to the wire.
i@nocollide // Collision detection for the edge is disabled (Only used if Collision Handling is SDF).
v@restP // Rest position of each point.
p@restorient// Rest orientation of each point.
i@gluetoanimation   // Causes a point’s position and orientation to be constrained to the input geometry.
i@pintoanimation    // Causes a point’s position to be constrained to the input geometry.
v@animationP// Target position of each point.
p@animationorient   // Target orientation of each point.
v@animationv// Target velocity of each point.
v@animationw// Target angular velocity of each point.
i@independentcollisionallowed   // Toggle external collisions (Only non-SDF Geometric Collision).
i@independentcollisionresolved  // Unresolved external collisions (Only non-SDF Geometric Collision).
i@codependentcollisionallowed   // Toggle soft body collisions (Only non-SDF Geometric Collision).
i@codependentcollisionresolved  // Unresolved toggle soft body collisions (Only non-SDF Geometric Collision).
i@selfcollisionallowed  // Toggle self collisions (Only non-SDF Geometric Collision).
i@selfcollisionresolved // Unresolved toggle self collisions (Only non-SDF Geometric Collision).
```

_DOP FLIP Attributes_<br />
The FLIP Solver contains an embedded POP Solver, enabling the use of many POP attributes.
```
f@pscale// Particle scale
v@v     // Particle velocity
f@viscosity // The "thickness" of a fluid.
f@density   // The mass per unit volume.
f@temperature   // The temperature of the fluid.
f@vorticity // Measures the amount of circulation in the fluid.
f@divergence// Positive values cause particles to spread out, negative cause them to clump together.
v@rest  // Used to track the position of the fluid over time.
v@rest2 // Used for blending dual rest attributes, avoids stretching.
f@droplet   // Identifies particles that separate from the main body of fluid.
f@underresolved // Particles that haven't fully resolved on the grid.
i@ballistic // Specifies particles which will be ignored by the fluid solve.
v@Lx    // Angular momentum X axis
v@Ly    // Angular momentum Y axis
v@Lz    // Angular momentum Z axis
```
