# greatunihack2021
Reinforcement Learning. Retro theme.

- Overview, set the theme, and intro links

We suggest suggest retro theme, but two things:
* Retro doesn't just mean retro video games. 
* Even more, we are looking for inovative RL applications. If your idea isn't retro, you can still impress us!

## Places to start

What is Reinforcement Learning ([link1](https://www.geeksforgeeks.org/what-is-reinforcement-learning/), [link2](https://towardsdatascience.com/reinforcement-learning-101-e24b50e1d292))?

OpenAI gym provides a bunch of [test environments](https://gym.openai.com/envs/#classic_control) for playing around with RL. You can even make your [own environments](https://towardsdatascience.com/creating-a-custom-openai-gym-environment-for-stock-trading-be532be3910e) using their library!

```python
import gym
from gym import spaces

class CustomEnv(gym.Env):
  """Custom Environment that follows gym interface"""
  metadata = {'render.modes': ['human']}

  def __init__(self, arg1, arg2, ...):
    super(CustomEnv, self).__init__()
    # Define action and observation space
    # They must be gym.spaces objects
    # Example when using discrete actions:
    self.action_space = spaces.Discrete(N_DISCRETE_ACTIONS)
    # Example for using image as input:
    self.observation_space = spaces.Box(low=0, high=255, shape=
                    (HEIGHT, WIDTH, N_CHANNELS), dtype=np.uint8)

  def step(self, action):
    # Execute one time step within the environment
    ...
  def reset(self):
    # Reset the state of the environment to an initial state
    ...
  def render(self, mode='human', close=False):
    # Render the environment to the screen
    ...
```
[Keras RL examples](https://pytorch.org/tutorials/intermediate/reinforcement_q_learning.html) may be a good starting point for training the models 

Feel free to a look at other Reinforcement Learning libraries (it doesn't have to be Python), there are plenty out there.   



## Judging criteria:
* Creativity of task

Creativity of a solution or a task that a model will perform. If you need to (or want to!) use something complex like state-of-the-art Deep RL neural nets, go for it. However, simple AI solutions can solve facinating problems just as well.

* Theme

We suggest retro theme, but two things. But 



https://gym.openai.com/ -- provides plenty of environments for RL. Including some games like Pinball -- https://gym.openai.com/envs/VideoPinball-ram-v0/
A nice intro to Deep RL with pytorch (uses OpenAI Gym) -- https://pytorch.org/tutorials/intermediate/reinforcement_q_learning.html
These are the, pretty much, standard starting points for Deep RL. (edite


Also, as we are talking about retro-game-ish theme, maybe we can give some assets that we like, as an inspiration source? For example, I scrolled itch.io and liked this free pack https://v3x3d.itch.io/retro-lines

Further inspiration for RL, beyond the getting started:
Want to build a multiplayer game with RL?: https://medium.com/applied-data-science/how-to-train-ai-agents-to-play-multiplayer-games-using-self-play-deep-reinforcement-learning-247d0b440717
Want to use real hardware agents?: https://hackaday.com/2019/05/25/little-lamp-to-learn-longer-leaps/
Want to apply RL to 'retro' technologies (I know sailing is not quite retro, but I couldn't come up with a better example)?: https://github.com/PPierzc/ai-learns-to-sail
Want to nudge how an agent learns yourself (i.e. learning from human preference)? https://openai.com/blog/deep-reinforcement-learning-from-human-preferences/ [this one might be too ambitious for a hackathon though, but maybe the idea itself is inspirational enough?]
