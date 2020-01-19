# Hack Cambridge 2020

### Team Submission: A Multi-Agent's Paradise

### Authors:
- Joe Arrowsmith
- Sirvan
- Edward Stables
- Tudor Trita

### Devpost Subsmission:
- (https://devpost.com/software/a-multi-agent-s-paradise)


#### Inspiration for the idea:
- Using browser games as our inspiration for the style, we wanted to create a toy environment for the development of agents that can learn to cooperate and communicate.
- Research works such as Emergent Tool Use from Multi-Agent Interaction by OpenAI (Hide and Seek video) and RL networks such as DRQN (https://arxiv.org/pdf/1507.06527.pdf) were key in leading the project direction.

#### What does the program do?
- Game server that can take connections from both real players and AI agents. The intention is to use the game server in multi-agent training, with the plan to teach the agents the ability to communicate, hopefully generating their own language.
- In the theme of this year we wanted to build everything from the ground up as much as possible and even "attempt" to follow proper software development protocols. (Setup travis, unittests, git branches)

#### The Game:
- Teams of equal sizes are placed in a randomly generated world. They need to stay on the path and avoiding falling into the void or being trapped by the world map getting smaller. They can push other agents and "reinforce" their team mates by standing behind them and stopping them being pushed back, or help attack an enermy player at the same time.
- The last team alive wins the game!
- Agents are rewarded for their team performance, and intermidate rewards can be added in such as failing to respond to message of nearby friendlies.

#### How we built it?
- Python server backend, websockets for communicating between server backend and javascript frontent, tensorflow backend, also websockets between agents and server
- Making the python asyncio library do what you want, making a consistent environment that works for both ai and humans.
- Designing the network that reads and generates text within the time constraint.

- The game engine managed to get working with web UI and multiple clients

#### What did we achieve?
- Working with multi client systems in an asynchronous manner with two very different client types

#### Further steps for improvement:
- Implement standard baselines such as PPO, SAC, A3C
- Implement example network for reading and generation of messages
- Add functionality for mobile
- Add functionality for agents to communicate and to visualise the messages
