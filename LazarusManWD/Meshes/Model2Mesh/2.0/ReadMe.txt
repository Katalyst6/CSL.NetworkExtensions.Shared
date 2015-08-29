Model 2 Mesh
Latest Version: 2.0
Lazarus*Man

**Note:  This program is designed for those who are knowledgable in Unity.  If you are not, look up YouTube videos on procedural meshes.  This is a good video series to get an idea of what you are getting yourself into:

https://www.youtube.com/watch?v=3RlKf7Q8CYM

******************************************

This program is responsible for talking a mesh .OBJ file that you have created and making it into a procedural mesh that can be read by Unity (the engine behind CS).  To integrate your mesh:

1. Make your class file in the appropriate folder within the project
2. Open Model2Mesh and input the namespace and name of the class (these can be done later though).
3. Browse for your .OBJ file.  When you export your .OBJ, make sure:
	a. It is in trianges and not quads
	b. If applicable, optimize your normals and texture-coord (Not Vertices!)
4. Select the .OBJ file and click Open.
5.  Finally, hit the 'GO' button and copy the entire contents of the parser to your class file.  If you added your namespace path and class name, it should do everything else and you can simply paste it over what was already in the mesh class file.


Current Limitations:

1. This was a quick and humble tool I built to help in mesh creation.  It is not very pretty and might have some bugs.  Please be patient with it.
2. Model2Mesh maps vertices, triangles, and texture coordinates to the procedural mesh class.  Normals will have to be recalculated seperately by doing a RecalculateNormals() command after setting the properties of the GameObject you are originally trying to create/alter.
3. Model2Mesh does texture mapping on a x-y basis only.  It does not do well with mapping 3d Objects and therefore works best for flat meshes.  I will work more on this later.

Good Luck and Have Fun,
-Andre



v2.0: Added mesh type dropdown and autopopulation.  Accounted for some CSL solution structural changes.