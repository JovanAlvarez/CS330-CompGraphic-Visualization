The goal of the project was to recreate a realistic desk environment while demonstrating core graphics concepts including transformations, lighting, texturing, camera control, and scene management within C++/OpenGL. The rendered environment represents a desktop workspace containing a wooden desk surface, a coffee mug with a textured body and coffee surface, a stack of books and a notebook, and common desk peripherals such as a monitor, keyboard, and mouse. The scene supports full camera movement and includes custom materials and multiple light sources to enhance visual depth and realism.

-Project Overview-
The scene was constructed using modular managers for rendering and camera control. Each object is positioned using model transformations and rendered with either a texture or material color. Lighting calculations are handled in the shader and applied per object using configurable material properties.

Key capabilities implemented in this project include:
  Custom textured surfaces for the desk, mug, and coffee
  Per-object material settings including ambient, diffuse, specular, and shininess
  Multiple light sources to simulate key, fill, and ambient lighting
  Interactive camera movement with mouse-look and keyboard navigation
  Perspective and orthographic projection modes
  Depth testing and real-time rendering

-Scene Composition-
The environment includes a wooden desktop plane textured with a wood material. A coffee mug is constructed from multiple meshes, including a cylindrical body, a torus handle, and a thin cylinder representing the coffee surface. A stack of books and a notebook are created using scaled box meshes. The monitor is built from multiple components including a housing, screen inset, stand, and base. Additional peripherals include a keyboard and mouse positioned on the desk surface.
All objects are placed using translation, rotation, and scale transformations to recreate a realistic desktop layout.

-Camera and Controls-

The scene supports full free-look camera movement.

Keyboard controls:
  W and S move forward and backward
  A and D move left and right
  Q and E move up and down

Mouse movement controls camera rotation.
Mouse scroll adjusts camera behavior based on the camera implementation.

Projection controls:
  TAB toggles between perspective and orthographic projection
  P switches to perspective projection
  O switches to orthographic projection

Press ESC to exit the application.

-Lighting and Materials-
Lighting is enabled through the shader and applied using multiple light sources positioned around the scene. These lights simulate directional emphasis, fill lighting, and low-level ambient bounce. Each object uses a configurable material system that controls ambient strength, diffuse color, specular highlights, and shininess. Textured objects use UV scaling to control texture repetition and detail. This combination of lighting and materials improves surface definition and helps separate objects visually within the scene.

-Technologies Used-
Language: C++
Graphics API: OpenGL (Core Profile)
Window and input handling: GLFW
OpenGL extension loading: GLEW
Mathematics: GLM
Image loading: stb_image
Shaders: GLSL

The project was developed and tested in Visual Studio on Windows.

-Implementation Notes-
Depth testing is enabled to ensure proper object overlap. The render loop clears both color and depth buffers each frame. The view and projection matrices are updated every frame through the ViewManager. Each object follows a consistent workflow: apply transformations, send the model matrix to the shader, configure texture or color, apply material properties, and draw the mesh.

-Troubleshooting-
If textures appear black or missing, verify that the texture files are located in the correct directory and that filenames match exactly. If the scene appears unlit or too dark, review the lighting values defined in the scene lighting setup or adjust material shininess. If the display appears flat, confirm that perspective mode is active instead of orthographic projection.

-Academic Context-
This project was completed as part of SNHU’s CS-330 course to demonstrate understanding of 3D transformations, camera systems, lighting models, and real-time rendering techniques. The implementation reflects progressive development over multiple assignments and iterative scene refinement.
