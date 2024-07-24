# Cosmic Cafe

## Game Architecture
1. Orchestrator Node:
- Central hub for all communications
- Manages game flow, logic, and environmental factors
- Distributes tasks to agent nodes
- Collects and processes responses from agents
- Handles user input and output
- Generates and manages events

2. Agent Nodes (Zorp, Exra, Lumi, Chip):
- Each runs on a separate node
- Processes tasks sent by the orchestrator
- Sends responses only to the orchestrator
- Cannot communicate directly with other agents

## Game Introduction
Welcome to Cosmic Cafe, a quirky establishment at the edge of the universe where intergalactic beings gather to share stories, solve problems, and enjoy exotic refreshments.

As the overseer of this unique simulation, your task is to present a galactic problem that needs solving. Once introduced, you'll witness how the diverse patrons of Cosmic Cafe interact, combining their unique abilities and perspectives to address the challenge.

The fate of the galaxy rests in the hands (appendages, tentacles, or energy fields) of our eclectic cast:

- Zorp, the multi-limbed cafe owner with a knack for bringing people together
- Exra, a time-traveling historian with knowledge from across the ages
- Lumi, an empathic being who can sense and influence emotions
- Chip, a malfunctioning robot eager to understand organic life

Will their combined efforts lead to an ingenious solution, or will their quirks and misunderstandings complicate matters? Only time will tell in this cosmic simulation of problem-solving and interpersonal dynamics.

## Game Mechanics

1. Initialization:
Orchestrator loads agent profiles from YAML files
Orchestrator initializes each agent node with its profile

2. Problem Input:
User inputs the galactic problem to the orchestrator
Orchestrator analyzes the problem and prepares initial tasks

3. Task Distribution:
Orchestrator creates specific tasks for each agent based on their abilities
Tasks are sent to agent nodes one at a time

4. Agent Processing:
Agents process their assigned tasks
They respond to the orchestrator with their results or requests

5. Information Sharing:
If an agent needs information from another agent, it must request it through the orchestrator
Orchestrator decides whether to forward the request or provide information based on previous responses

6. Conversation and Event Simulation:
Orchestrator simulates conversations by sending relevant information to agents
Orchestrator generates events and distributes event-related tasks to relevant agents
Agents respond with their contributions, which the orchestrator then synthesizes

7. Solution Development:
Orchestrator breaks down the problem-solving process into subtasks
Subtasks are distributed to appropriate agents
Orchestrator compiles and synthesizes agent responses to form solution components

8. Consensus Building:
Orchestrator presents potential solutions to agents for evaluation
Agents provide feedback to the orchestrator
Orchestrator uses this feedback to refine the solution

9. Result Compilation:
Orchestrator gathers all processing data and solution components
Compiles a final report showcasing the problem-solving process and solution

## Example Interaction Flow:
Orchestrator Tasks:

1. Cosmic Awakening Phase:
Load and parse all YAML files (environment, agents)
Initialize agent nodes with their profiles
Set up the initial game state
Present the galactic problem to the user and receive input

2. Galactic Scan Phase:
Break down the user-input problem into initial tasks
Distribute initial analysis tasks to agents
Collect and synthesize agent responses
Update global variables based on initial analysis

3. Nebula Brainstorm Phase:
Generate and assign specific solution-oriented tasks to agents
Manage information requests between agents
Trigger and manage cosmic events from the environment
Collect and synthesize agent contributions
Start forming potential solutions

4. Stellar Refinement Phase:
Present initial solutions to agents for evaluation
Collect feedback and refine solutions
Manage any conflicts or disagreements between agents
Finalize the best solution(s)

5. Universal Convergence Phase:
Compile final results and solution
Generate a comprehensive report of the problem-solving process
Present the outcome to the user

6. Throughout All Phases:
Manage the progression of rounds within each phase
Handle transitions between phases
Monitor for timeout or max rounds reached
Handle agent node failures or non-responses
Update and maintain game state
Log all interactions and decisions for the final report