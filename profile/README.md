Open Engineering Tour

Open Engineering Tour is the implementation repository of the tour definitions from Open Engineering Tours.

A Tour turns an Open Engineering Architecture scene into an interactive visual journey.

Tours guide a viewer through a scene by moving step-by-step between one or more cameras. Each camera establishes a particular viewpoint, allowing an architectural scenario to be experienced as a sequence rather than as a single static diagram.

Purpose

Open Engineering Tour provides the implementation that brings Tour definitions to life.

It connects:

Tour Definition → Scene → Cameras → Steps → Viewer

A Tour can therefore describe a journey through an architectural scene such as:

* entering an environment
* approaching a system
* focusing on a component
* following a communication path
* examining an interaction
* revealing an architectural decision
* returning to an overview

The Tour definition describes what the journey is; this repository implements how the journey is executed.

Architecture

Open Engineering Tour is designed to work with the Open Engineering Architecture visualization stack.

Open Engineering Tours
        │
        │ Tour definitions
        ▼
Open Engineering Tour
        │
        ├── Tour
        ├── Steps
        ├── Camera selection
        ├── Camera transitions
        └── Viewer interaction
        │
        ▼
Open Engineering Architecture
        │
        ▼
Babylon.js Scene

The scene is created using Babylon.js and contains one or more cameras. A Tour selects those cameras in sequence and uses them to lead the viewer through the scene.

Tour

A Tour is a sequence of viewpoints through a scene.

Conceptually:

Tour
 ├── Step 1 → Camera A
 ├── Step 2 → Camera B
 ├── Step 3 → Camera C
 └── Step 4 → Camera D

Each step changes the viewer’s perspective and can establish the context required for the next part of the story.

This makes Tours a natural bridge between architectural models and visual storytelling.

Definitions and Implementation

Open Engineering separates definitions from their implementations.

Repository	Responsibility
Open Engineering Tours	Defines Tours
Open Engineering Tour	Implements Tours

This separation allows Tour definitions to remain declarative and reusable while the implementation evolves independently.

Relationship to Scenes

A Tour does not replace an architectural scene.

Instead, it provides a guided projection through the scene.

Architecture
     │
     ▼
   Scene
     │
     ├── Camera 1
     ├── Camera 2
     ├── Camera 3
     └── Camera 4
          ▲
          │
        Tour

The same scene can therefore support multiple Tours.

For example, one scene could provide:

Architecture Overview
System Interaction
Deployment Journey
Data Flow
Security Journey

Each Tour can tell a different story using the same underlying architectural environment.

Babylon.js

Open Engineering Tour uses Babylon.js as the 3D scene runtime.

Babylon.js provides the foundation for:

* 3D scenes
* cameras
* meshes
* materials
* animation
* lighting
* interaction

Open Engineering Tour adds the concept of a guided camera journey on top of that scene.

Design Principles

Definitions first

Tour behavior should originate from explicit definitions rather than being hidden inside application code.

Reuse the scene

Tours should navigate existing architectural scenes instead of creating parallel representations of the architecture.

Cameras are viewpoints

A camera represents a meaningful architectural viewpoint, not merely a technical camera position.

Steps tell a story

Each step should contribute to the viewer’s understanding of the scenario.

Implementation remains replaceable

The definition of a Tour should remain independent from the particular implementation used to render it.

Open Engineering Ecosystem

Open Engineering Tour is part of the broader Open Engineering ecosystem.

Open Engineering
       │
       ├── Architecture
       │      │
       │      └── Scenes
       │
       ├── Tours
       │      │
       │      └── Tour definitions
       │
       └── Tour
              │
              └── Tour implementation
                       │
                       ▼
                   Babylon.js

The result is an architectural experience in which a model can be explored not only spatially, but also temporally.

Philosophy

A diagram shows where things are.
A Tour shows how to look at them.

Open Engineering Tour turns architectural visualization into a guided experience — helping viewers understand complex systems by revealing the architecture one viewpoint at a time.

⸻

Open Engineering Tour
The implementation of Open Engineering Tours.
