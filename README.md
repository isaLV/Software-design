# Software-design





Architecture/Design Document
For
Paint++

v1.0
















Prepared by: Blake Stinson, Andrew Swanson, Joey Truszinski, Lissette Velec
Table of Contents
Introduction	2
Design Goals	4
System Behavior	4
Logical View	4
High-Level Design (Architecture)	5
Mid-Level Design	5
Detailed Class Design	6
Process View	7
Development View	8
Physical View	9
Use Case View	9
Team Work	9
Work completed by Blake Stinson	9
Work completed by Andrew Swanson	10
Work completed by Joey Truszinski	10
Work completed by Lissette Velec	10


Revision History
Version
Date
Name
Description
v1.0
Paint++
We created the initial Software Design Document











Introduction

This document describes the architecture and design for the Paint++ application being developed for all users. Our application, Paint++, is a remake of the popular Microsoft Windows software Microsoft Paint. It will have many of the features Paint does, primarily being able to “paint” your own artwork.

The purpose of this document is to describe the architecture and design of the Paint++ application in a way that addresses the interests and concerns of all major stakeholders. For this application the major stakeholders are:

Users – they want assurances that the architecture will provide for system functionality and exhibit desirable non-functional quality requirements such as usability, reliability, etc.
Developers – they want an architecture that will minimize complexity and development effort.

The architecture and design for a software system is complex and individual stakeholders often have specialized interests. There is no one diagram or model that can easily express a system’s architecture and design. For this reason, software architecture and design is often presented in terms of multiple views or perspectives [IEEE Std. 1471]. Here the architecture of the Paint++ application is described from 4+1 different perspectives [1995 Krutchen]:

Logical View – major components, their attributes and operations. This view also includes relationships between components and their interactions. When doing OO design, class diagrams and sequence diagrams are often used to express the logical view.
Process View – the threads of control and processes used to execute the operations identified in the logical view.
Development View – how system modules map to development organization.
Physical View – shows the system hardware and how software components are distributed across the processors in the system. 
Use Case View – the use case view is used to both motivate and validate design activity. At the start of design the requirements define the functional objectives for the design. Use cases are also used to validate suggested designs. It should be possible to walk through a use case scenario and follow the interaction between high-level components. The components should have all the necessary behavior to conceptually execute a use case.
Design Goals
Designs goals it’s a basic toolbar which consists of creating background classes with background colors etc. In that tool bar we have different types of bottoms or items to click, with different components for the paint ++. We have black canvas windows with different sizes and different types of colors of the paint++
In use cases it’s the behavior on the project we work on
·         Handles multiple users at the same time
·         Support for both public and private messages
·         With the ability of the drawing point data
System Behavior
System behavior its cause from a state to another, and the actions will be represented in our history of our program. E.g we implemented action listeners  we declare some names some arrays and  we starts we state marked by triggers this indicate how our system behave one state to another state.
·         Interaction / Display images
·         State with the machine
·         Organization 
·         Grouping
·         anotation


Logical View
The logical view describes the main functional components of the system. This includes modules and the static relationships between modules. 

In this section the modules of the system are first expressed in terms of high level components (architecture) and progressively refined into more detailed components and eventually classes with specific attributes and operations.


High-Level Design (Architecture)

Figure 1: A High level diagram showing the different components of the project. A general workflow of how the user will interact is shown.

The high-level view or architecture consists of 3 major components:

The Application
The Application is what hosts every component inside it, and allows the user to resize the application and close it.
The Toolbar
The Toolbar hosts all of the drawing options that the user can select. The user can use buttons to switch drawing color, switch drawing modes, switch brush size and save their final drawing.
The Canvas
The canvas is where the user interacts with their mouse to draw different shapes and do different drawing related things.













Mid-Level Design
The Application hosts the Toolbar and the Canvas. The toolbar controls the different colors, shapes and drawing tools that the user can select. When the user interacts with the toolbar, the behavior of the Draw class will be updated to the selected configuration. The toolbar uses a ButtonFactory to create buttons of certain styles for different tools/colors/modes etc.



Figure 2: A mid level UML class diagram depicting the classes related to the application that the user will interact with



Detailed Class Design


Figure 3: A detailed UML class diagram depicting the classes and their variables and methods that will be implemented
Process View

In this UML Diagram as seen in Figure 3 we see the following classes, Main, Application, Toolbar, and Canvas. In this diagram we are showing that Main creates the new Application. In the application class we can see that it will first create a new toolbar using the toolbar class. Then the application class will create a new canvas that the user can draw on by using the canvas class. 









Figure 3: A UML sequence diagram showing the process of how our Paint++ application runs.
Development View
In the project we used one programming language which was java and used a few different libraries. The libraries that we have used are the abstract window toolkit, and swing. The library used to create the window was swing by using Jframes and Jpanels. Inside of these frames and panels are labels to display text. The next library used was the abstract window toolkit, which was used to create the dimensions, colors and functionalities of our toolbar and canvas. For the testing purposes of this software (As seen in figure 4) we are going to be testing the most common and most important functionalities, and these include drawing with different colors, clearing the canvas, and selecting different drawing stroke sizes. 


Figure 4: A project decomposition diagram showing how we will check the main functionalities of the program. 

Physical View
Our project’s physical view is pretty straightforward, especially considering it runs all on one device. As shown below in Figure 5, the user uses the mouse to interact with the application. This has the CPU process the inputs and send instructions to the GPU to render. The GPU renders that to the monitor, which gives information back to the user.



Figure 5: A box and line diagram that portrays how the system components interact.
Use Case View

UC-1 - Turn on the grid and resize the canvas to the wanted size.
For our first use case, we have the ability to turn on a grid and resize the canvas through the toolbar. This was implemented via our ButtonFactory class, and is used in our toolbar class, which is instantiated in our Application class, which is created in our Main class.
UC-2 - Select a tool to paint or draw with.
For our second use case, we have the ability to select a tool to paint or draw with via the toolbar in the application. This was implemented via our ButtonFactory class, which is used in our toolbar class. The toolbar is, as with UC-1, instantiated in our Application class, which is created in our Main class.
UC-3 - Select a color to create a drawing on canvas.
For our third use case, we have the ability to select a color that changes the color of our tools. We implemented a color picker and a set of default colors to choose from. This is implemented via the ButtonFactory class, which is used in our toolbar class. The toolbar is, as with UC-1, instantiated in our Application class, which is created in our Main class.
UC-4 - Save the masterpiece that was created.
For our fourth use case, we have the ability to save the masterpiece that was created. This is located in the toolbar on our application’s window. This is implemented via our ButtonFactory class, which is used in our toolbar class. The toolbar is, as with UC-1, instantiated in our Application class, which is created in our Main class.


Completed Work
Added drawing functionality
Added different colors
Added different stroke sizes
Added different tools
Added ability to save work

Team Work
Work completed by Blake Stinson
Introduction
Physical View
UC-1
Work completed by Andrew Swanson
System Behavior
Logical View
UC-2
Work completed by Joey Truszinski
Process View
Development View
UC-3
Work completed by Lissette Velec
Introduction
Design Goals
UC-4


