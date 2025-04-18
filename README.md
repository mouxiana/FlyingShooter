# 🚀 FlyingShooter - Python 

<div align="center">
 <img src="https://github.com/mouxiana/FlyingShooter/raw/master/Screenshots/gameplay.gif" width="600" alt="Game Demo">

 [![Python 3.10+](https://img.shields.io/badge/Python-3.10%2B-blue)](https://www.python.org/)
 [![PyGame 2.0](https://img.shields.io/badge/PyGame-2.0-red)](https://www.pygame.org/)
 [![License: MIT](https://img.shields.io/badge/License-MIT-green)](LICENSE) [![EXE download](https://img.shields.io/badge/Download-EXE-brightgreen)](https://github.com/mouxiana/FlyingShooter/releases/latest)
</div>

## 🎮 Game introduction
2D flying shooting game developed using Python+PyGame, including the following features:
- Three weapon systems: machine gun
- Dynamic difficulty system: increase enemy strength with score and time
- Local leaderboard: save the highest score record
- Keyboard dual control mode
 

## 💻 Quick start

### Run mode 
#### Method: Run EXE directly
1. Download `FlyingShooter_v1.0.exe` from the [Release page](https://github.com/mouxiana/FlyingShooter/releases)
2. Double-click to run (no need to install Python environment)

## Directory Structure
src(core code directory): 
- game.py

## YouTube Demo
Youtube Demo: https://youtu.be/9r7MmCejQNA?si=XdtjEGpi3VIgbzHE

## Graphical Abstract
<img width="1280" alt="40ad47db7ecb40326739b484d199778" src="https://github.com/user-attachments/assets/e75e8229-80cf-4e3b-a8a6-c288be347b17" />


## Product Positioning
This product is mainly aimed at students and aims to create a competitive shooting game that supports online multi-player gameplay.The development is divided into two phases:
- Initial stage: focus on core function implementation
  - Single player game
  - Record the top three highest scores in history
  - Basic gameplay
- Long-term plan: increase gameplay, design more modes, open online competitive gameplay, design more enemies and player-controlled characters, and improve player playability.

## Target users and development process
- Target Market: Student Group
- SW development process: Agile process
- Reason to choose Agile:
  - Adapting to rapidly changing market demands：Changing market trends，Agile development can quickly adjust game content and functions through short-cycle iterations, keep up with market changes, and seize opportunities.
  - Improve development efficiency and shorten time to market: Agile development emphasizes the rapid construction of game prototypes, obtaining player feedback through early testing, promptly identifying problems and making improvements, and avoiding large-scale rework later.
  - Improve game quality and player satisfaction: In each iteration, we focus on improving and optimizing specific features to ensure higher overall quality of the game.
  - Encourage innovation and adaption to new technologies: Mini games need to keep innovating to attract players. Agile development encourages teams to try new ideas and gameplay, and quickly verify and launch new features.
  - Enhance team collaboration and communication: Mini game development requires close collaboration among different roles such as planning, programming, and art. Agile development encourages communication and collaboration among team members to improve work efficiency.Team members can promptly understand project progress and issues, thus enhancing team cohesion and execution.
- Therefore, based on these characteristics, Agile is more suitable.

## Planning Overview
### Development Process
- Week 1: Concept, Planning, and Initial Design
  - Game Concept Definition：Finalizing the game concept, target audience, and core mechanics.
  - Storyboarding: Selecting appropriate technologies and frameworks for the game.
  - Creating a Sprint Backlog: Prioritizing tasks for the first sprint, including initial coding and design work.
- Week 2: Game Engine Setup and underlying Code Development
  - Underlying Code Development: Writing the basic game logic, input handling, and core functionality.
  - Initial Asset Creation: Starting to design and create basic game assets like sprites and backgrounds.
  - Daily Stand-ups and Progress Review: Ensuring the team is on track and addressing any issues.
- Week 3: Iterative Development and Testing
   - Feature Development: Implementing key game features and mechanics.
   - Integration of Game Assets: Integrating designed assets into the game engine.
   - Testing and Debugging: Conducting unit testing and identifying bugs for resolution.
   - Feedback Integration: Incorporating feedback from team members and early playtesters.
- week 4:Game balance and optimization
   - Game Balancing: Tweaking game mechanics for better player experience and difficulty level.
   - Polishing: Enhancing visual and audio elements, improving overall game performance.
   - Software packaging preparation: Begin software packaging preparation, including creating installation files and testing on different platforms.
- week 5:Final testing, packaging, and release preparation
   - Comprehensive Testing:  Conducting thorough testing across various devices and platforms to ensure stability and functionality.
   - Bug Fixing: Addressing any remaining issues identified during testing.
   - Software Packaging and Submission: Complete the software packaging process in preparation for release on the app store
   - Release Planning: Prepare marketing materials, release notes, and finalize the release plan.
   - Final Review: Conduct a final review with the team and stakeholders before release.

- Requirement Specification:
   - **Initial Vision**: Define the game's vision, target audience, and core gameplay concepts.
   - **User Stories**: Create user stories that outline the features and functionality required.
   - **Product Backlog**: Prioritize user stories in the product backlog based on importance and feasibility.
- Design and Development:
   - **Sprint Planning**: Plan each sprint by selecting user stories from the product backlog.
   - **Design Iterations**: Design game mechanics, user interface, and visual elements in short cycles.
   - **Coding**: Develop the game in small, manageable increments, focusing on one feature at a time.
   - **Continuous Integration**: Integrate new code regularly to ensure compatibility and stability.
- Testing and Validation:
   - **Unit Testing**: Test individual components of the game as they are developed.
   - **Integration Testing**: Test how different parts of the game work together.
   - **User Acceptance Testing**: Gather feedback from users and make necessary adjustments.
   - **Bug Fixing**: Address issues identified during testing.
- Maintain and Evolution
   - **Release Planning**: Prepare the game for release, including final testing and polishing.
   - **Post-release Monitoring**: Monitor user feedback and analytics after the game is released.
   - **Continuous Improvement**: Implement updates and new features based on user feedback.
   - **Bug Fixes and Updates**: Regularly update the game to fix bugs and improve performance.
- Iterative Development Cycle:
   - **Sprint Review**: At the end of each sprint, review the completed work and gather feedback.
   - **Sprint Retrospective**: Reflect on the sprint process, identify areas for improvement, and adjust for the next sprint.
   - **Adaptation**: Use feedback to adapt and refine the product backlog for future sprints.
 
### Schedule
Our product development process is iterative: user requirements specification-->design and development-->test verification-->release-->new user requirements-->design and development-->test verification-->release-->new user requirements-->design and development-->test verification-->release

### Members
- A product manager: Chord Lee
- A Tech Lead: Brian Lei
- A Act designer: Thomas Ng
- A Python Developer: Matthew Wang

### Algorithm explanations
- Dynamic enemy spawning system:
  - Weight distribution based on probability (C-level enemy aircraft 1/10, B-level 3/10, A-level 6/10)
  - The score affects the spawn probability linearly (every 1000 points increases the probability by 10%)
- Ballistic calculation system
  - Use the inverse tangent function to calculate the relative angle between the player and the enemy
  - Support angle offset to achieve fan-shaped barrage (-15°, 0°, +15°)
- Collision Detection System
  - Use PyGame's built-in Rect.colliderect() method
  - Object pool to manage bullet instances (avoid frequent creation/destruction of objects)

### Open Source Components List
- Core dependency libraries
  - Package    Version    Purpose
  - PyGame     ≥2.0       Graphics rendering/sound effects/input processing
  - Python     3.10+      runtime environment
- Development Toolchain
  - Tool Usage    Open Source
  - PyInstaller   EXE Packaging
  - pytest        unit testing
- Resource Files
  -  Font file: Pixeloid.ttf (developed by Sizenove Studio) - free commercial license
  -  Sound effect: fileshoot.wav/explosion.wav (CC0 protocol, source kenney.nl)
 
### System requirements
- Minimum hardware configuration
  - Component       Requirements
  - CPU             x86 dual-core 1.5GHz+
  - Memory          512MB RAM
  - Graphics card   supports OpenGL 2.0
  - Storage         50MB free space
- Software environment
  - System          Requirements
  - Windows         7 SP1+
  
 
### Full dependency installation
- Create requirements.txt:
  - pygame==2.5.0 numpy==1.26.4  (If you need to expand data analysis functions)
- Installation command:
  - pip install -r requirements.txt

### Architecture optimization suggestions
- ECS architecture transformation
  - Refactor existing code to the Entity-Component-System pattern
- Performance Optimization
  - Add frame rate control and load monitoring
- Cross-platform support
  - Use sys.platform to detect the system type

### Current status of the game
- Currently in beta 3.0.
- The official version will be released soon in the future
  
### Future plan
**Future plans**
- In the future, we hope to provide customized features to meet the needs of different users. For example, add more interesting enemies, add more skills to our characters, launch multiplayer mode to meet the needs of players playing with friends, and add more types of modes.
In addition, we plan to support more platforms in the future, such as Mac, IOS and Android
