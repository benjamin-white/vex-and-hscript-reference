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

**@accel** <br/>
**@center** <br/>
**@dPdx** <br/>
**@dPdy** <br/>
**@dPdz** <br/>
**@scale** <br/>
**@force** <br/>
**@rest** <br/>
**@torque** <br/>
**@up** <br/>
**@uv** <br/>
**@v** <br/>
**@backtrack** <br />
**@orient** <br />
**@rot** <br />
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
