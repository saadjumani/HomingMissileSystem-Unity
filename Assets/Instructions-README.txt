Part 1) Setting up the homing missile.

i) Import 3D model of missile into the scene. make sure missile is pointed straight along the Z Axis when rotation is 0,0,0.
ii) Browse to Assets/Homing_Missile folder, select HomingMissile script and attach to the missile.
iii) Adjust speed and maneuverability variables as per need from inspector penal. Leave them to default value if it feels confusing.
iv) [optional: you can skip this] If you need explosion effect, select your explosion prefab. This unity package comes with a very rudementary explosion prefab, feel free to use it if suitable. Otherwise unity standard assets has very good explosion prefabs too. Set it to none if no explosion is needed.
v) After all is done, make a prefab of the missile by dragging it from Hierarchy penal to assets penal.

Part 2) Setting up a launcher/turret
i) Import 3D model of your missile launcher into the scene.
ii) Browse to Assets/Homing_Missile folder, and add launcher script to the launcher object.
iii) From inspector penal, set Missile Prefab to the prefab you made in part 1.
iv) [optional: You can skip this, but it may look wierd.] If you don't want to finetune the position from where the missile is spawned:
	a) create an empty gameObject and call it Spawn Point (or any name you are comfortable with).
	b) place it at precise location from where you want to spawn the missile.
	c) Select the launcher object, and from inspector penal, set Spawn Point to the empty game object you just created. Now missile will be spawned from that exact place.

At this point, your launcher is ready to shoot missiles, all you need now is to set up conditions where launcher may be shot.

Part 3) Adding turret functionality.
i) Browse to Assets/Homing_missile folder, and add TurretFunction script to the launcher.
ii) From the inspector penal, enter the tag which will be used to identify the targets to be shot down.

If you wish to modify the script, keep in mind that launchMissile(target) function in Launcher.cs is what calls the object to fire, where target is the targeted gameObject.



