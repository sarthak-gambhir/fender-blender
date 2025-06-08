# Blender

## Mesh

In 3D modeling, a mesh is a collection of vertices, edges, and faces that define
the shape of a 3D object. It’s the fundamental building block for digital 3D
geometry, used in applications like game development, animation, 3D printing,
and simulation.

Here’s how a mesh is structured:

- Vertices: Individual points in 3D space.
- Edges: Lines connecting two vertices.
- Faces: Flat surfaces created by connecting three or more vertices (typically
  polygons, usually triangles or quads).
- Topology: The arrangement of vertices, edges, and faces, which affects the
  object’s structure and deformation capabilities.

Meshes can vary from low-poly (fewer faces for performance efficiency in games)
to high-poly (detailed models for cinematic or sculpting purposes). Proper mesh
optimization ensures smooth performance and effective rendering.

### Basic shapes

Ref - `basic-shapes.blend`

In object mode press `Shift + A` to add a mesh. Some basic 3D shapes/meshes are
provided out of the box like:

- Cube - Can be scaled to create a cuboid.
- Cylinder
- Cone
- Icosphere - Made from equilateral triangles with less amount of faces
- Sphere - Natural with more faces
- Torus - Circular loop

### Derived shapes

Ref - `basic-shapes.blend`

Some shapes can be derived out of basic meshes provided by blender.

- Pyramid (Square base)

  - Add a Cube.
  - Go into edit mode.
  - Move 4 vertices of the top face of the cube to the center

- Tetrahedron (Pyramid triangular base)

  - Add a Cube
  - Go into edit mode.
  - Move 4 vertices of the top face of the cube to the center
  - Merge 2 of the neighbouring base vertices.
  - Relocate vertices as per math

- Triangular prism (ramp)

  - Add a Cube
  - Go into edit mode.
  - Merge 2 neigbouring vertices of one face to the parallel edge.

- Star tetrahedron (Merkaba)
  - Create 2 tetrahedron
  - Rotate one to 180 degrees and arrange to make edge come out of the center of
    the faces of the other tetrahedron.
  - Press `Ctrl + J` to join the meshes.

## Modifiers

### Boolean modifier

The **Boolean Modifier** in Blender allows users to combine multiple meshes
using Boolean operations. It is a powerful tool for modeling complex shapes by
performing operations like **Union**, **Difference**, and **Intersect**.

#### Boolean Operations

- **Union**: Combines two objects into one, merging their geometry.
- **Difference**: Subtracts one object from another, creating a cutout.
- **Intersect**: Keeps only the overlapping volume of the objects.

#### Operand Types

- **Object**: Uses a single mesh object as the source.
- **Collection**: Uses multiple objects from a collection.

#### Solver Options

- **Fast**: Provides quick results but lacks support for overlapping geometry.
- **Exact**: More accurate but computationally expensive.

#### Additional Features

- **Self-Intersection Handling**: Improves results when objects intersect
  themselves.
- **Hole Tolerant Mode**: Optimizes Boolean operations for non-manifold
  geometry.
- **Material Transfer**: Allows materials to be mapped from the source object.

#### How to Use

1. Select the object you want to modify.
2. Go to the **Modifiers** tab (wrench icon).
3. Click **Add Modifier** and choose **Boolean**.
4. Set the **Operation** type (Union, Difference, or Intersect).
5. Select the **Operand Object** or **Collection**.
6. Adjust solver settings for better results.
7. Apply the modifier when satisfied.
