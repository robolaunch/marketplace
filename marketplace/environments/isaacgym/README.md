# <img src="https://www.svgrepo.com/show/331511/nvidia.svg" width="40" height="40" align="top"> NVIDIA Isaac Gym

NVIDIA’s physics simulation environment for reinforcement learning research.

Isaac Gym features include:

- Support for importing URDF and MJCF files with automatic convex decomposition of imported 3D meshes for physical simulation
- GPU accelerated tensor API for evaluating environment state and applying actions
- Support for a variety of environment sensors - position, velocity, force, torque, etc
- Runtime domain randomization of physics parameters
- Jacobian / inverse kinematics support

## How can you start Isaac Gym?

To start training of ANYmal C in Isaac Gym, open a new terminal and run the command below:

```bash
python3 /var/lib/repositories/legged_gym/legged_gym/train.py
```