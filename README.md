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

-Design Reflection-
1. How I Approach Designing Software

My approach to software design begins with defining the overall structure before writing detailed implementation code. For this project, I first broke the scene into logical components such as camera control, scene management, lighting, and object rendering. Separating responsibilities between the SceneManager and ViewManager helped keep the system organized and made it easier to expand the project over time.

One new design skill I developed during this project was thinking in terms of spatial composition and visual hierarchy. Instead of focusing only on functionality, I had to consider object scale, relative positioning, lighting direction, and material contrast to create a believable scene. This required planning the scene layout and adjusting transformations iteratively to achieve visual balance.

The design process I followed was incremental and modular. I began with a basic scene and camera, then progressively added objects, textures, materials, and lighting. Each feature was added in isolation and tested before moving forward. This approach reduced debugging complexity and allowed me to refine the scene without breaking existing functionality.

These design tactics will apply directly to future projects. Breaking systems into manageable components, separating responsibilities, and designing incrementally are practices that improve maintainability and scalability in both graphics applications and general software development.

2. How I Approach Developing Programs

My development strategy for this project focused on small, testable changes with frequent iteration. Instead of implementing large features at once, I added one object or capability at a time, compiled and ran the program, and visually verified the results. This was especially important in a graphics environment where issues such as incorrect transforms, lighting errors, or texture problems are easier to diagnose when changes are isolated.

New development strategies I used included:
  Building objects using reusable transformation patterns
  Testing lighting and material changes visually after each adjustment
  Using console output and incremental rendering to confirm resource loading and initialization

Iteration played a major role in the project. Many elements such as camera positioning, object scale, lighting intensity, and texture alignment required multiple adjustments before producing the desired result. Each milestone built on the previous one, gradually improving both functionality and visual quality.

Over the course of the project, my approach evolved from simply making features work to refining structure and readability. I became more intentional about organizing rendering code, grouping related operations, and maintaining consistency in how objects were configured. This shift toward cleaner structure reflects a more disciplined development process that will carry forward into future coursework and professional work.

3. How Computer Science Supports My Goals

This project strengthened my understanding of how mathematical and computational concepts translate into real-time visual systems. Working with transformation matrices, camera projections, lighting models, and shader communication reinforced core concepts from linear algebra and system design.

From an educational perspective, computational graphics has improved my ability to think in terms of coordinate systems, spatial reasoning, and performance-aware rendering. These skills support future coursework in areas such as simulation, visualization, and advanced software engineering.

From a professional standpoint, this experience builds skills that extend beyond graphics. The project required modular architecture, resource management, debugging complex runtime behavior, and iterative refinement. These are directly applicable to my long-term goals in software development and technical fields such as cybersecurity and AI, where system structure, performance awareness, and disciplined development practices are critical.
