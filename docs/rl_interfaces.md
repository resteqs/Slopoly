# RL Interfaces

**TBU**

Contract between the on-policy actor-critic (PPO) components so each module can be implemented and tested in parallel.

## Pipeline Overview

```text
[Engine] ---> (1. Learner transition) ---> [Collector] ---> (2. Rollout batch) ---> [GAE / Update]
                                                |                                         |
                                           (3. Policy) <----------------------------------+
                                                |
[Evaluation] <--- (5. Player) <-----------------+
                                                
[Reward] ---> (4. Reward) ---> [Collector / GAE]
[Config] ---> (6. Config) ---> [All Components]