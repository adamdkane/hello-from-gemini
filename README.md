# Git-Based, Collaborative, Agent-Driven Text Adventure Game

This project is a concept for a text adventure game that uses a Git repository as its foundation, with a Gemini agent acting as the game master. It's designed to test the capabilities of a coding agent in a dynamic, interactive, and creative environment.

## The Core Concept

The game world is represented by a directory structure within a Git repository. Each directory is a "room," and each room contains a `description.md` file that describes the room to the player. The player's current location is stored in a `player_location.txt` file.

Players interact with the game by creating issues in the repository. The title of the issue represents the player's command (e.g., "Go North," "Take the key," "Look around").

## The Agent's Role (Game Master)

The Gemini agent is the heart of the game. It continuously monitors the repository for new issues and acts as the "game master" by:

1.  **Processing Player Actions:** When a new issue is created, the agent reads the issue title to understand the player's command.

2.  **Updating Game State:** Based on the command, the agent updates the game state. This involves:
    *   Modifying the `player_location.txt` file to move the player to a new room.
    *   Creating or deleting files to represent items being taken or dropped.
    *   Modifying `description.md` files to reflect changes in the room.

3.  **Providing Feedback:** After processing the command, the agent comments on the issue with the result of the action. This would typically be the description of the new room, a confirmation that an item has been taken, or an error message if the command is invalid.

4.  **Closing the Loop:** Once the action is complete and feedback is provided, the agent closes the issue.

## Agent-Driven World Building

A key feature of this project is the agent's ability to expand the game world. Players can create issues with commands like "Create a new room to the east called 'The Library'." The agent would then:

1.  Create a new subdirectory named `library`.
2.  Use its creative capabilities to generate a description for the new room.
3.  Create a `description.md` file in the `library` directory with the generated description.
4.  Update the `description.md` of the current room to mention the new exit to the east.

## Why This is a Good Test for Gemini Agents

This project pushes the boundaries of what a coding agent can do by testing a wide range of capabilities:

*   **File I/O:** The agent must be able to read, write, and create files and directories.
*   **Git Integration:** The agent needs to interact with a Git repository in a meaningful way, including reading and commenting on issues, and pushing file changes.
*   **Natural Language Understanding:** The agent must understand the player's commands, which are expressed in natural language.
*   **State Management:** The agent is responsible for maintaining the state of the game world and the player's location within it.
*   **Creativity and Content Generation:** The agent can be used to generate creative and engaging content for the game world.
*   **Multi-step, Autonomous Tasks:** A single player command can trigger a complex sequence of actions that the agent must carry out autonomously.
*   **Collaborative Environment:** The project can be extended to support multiple players, which would require the agent to handle potential conflicts and manage a more complex game state.

This project provides a rich and engaging environment for testing and developing the capabilities of Gemini agents, pushing them beyond simple code generation and into the realm of interactive, creative, and autonomous problem-solving.
