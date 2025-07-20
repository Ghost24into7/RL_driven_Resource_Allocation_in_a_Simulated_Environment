# 🚀 ResourceMaster: Dynamic Resource Allocation with Reinforcement Learning 🌌

Welcome to **ResourceMaster**, an innovative project that harnesses the power of Reinforcement Learning (RL) to tackle the complex challenge of resource allocation in a simulated environment! This project pushes boundaries by simulating a dynamic system where tasks demand CPU and memory resources, and an RL agent learns to optimize allocation in real-time. Built with Python, Stable-Baselines3, and an interactive visualization powered by Matplotlib and Jupyter widgets, ResourceMaster is both a technical marvel and a learning playground for RL enthusiasts.

---

## 🌟 **What is ResourceMaster?**

Imagine a bustling digital factory where tasks arrive unpredictably, each demanding a slice of CPU and memory. ResourceMaster is a simulated environment where a Proximal Policy Optimization (PPO) agent learns to juggle these demands, making split-second decisions to allocate resources efficiently. The goal? Maximize task completion while minimizing resource waste. With a sleek, interactive visualization, you can watch the agent in action, tweaking parameters like task arrival rates and resource capacities to see how it adapts.

This isn't just code—it's a window into the future of intelligent resource management, from cloud computing to IoT systems.

---

## 🎨 **Features That Shine**

- **Dynamic Environment**: A custom Gym environment simulates task arrivals with configurable CPU and memory demands, controlled by a probability parameter `p`.
- **Smart RL Agent**: Powered by Stable-Baselines3's PPO algorithm, the agent learns optimal resource allocation strategies over 100,000 timesteps.
- **Interactive Visualization**: Real-time bar charts and trend plots showcase CPU/memory loads and cumulative rewards, with annotations for new tasks and completions.
- **Tunable Parameters**: Adjust task arrival probability, CPU, and memory capacities via sliders for a hands-on experience.
- **GPU Acceleration**: Leverages CUDA (when available) for faster training, with fallback to CPU for accessibility.
- **Performance Insights**: Evaluate the agent's performance with mean and standard deviation of rewards over multiple episodes.

---

## 🛠️ **Getting Started**

### Prerequisites
To dive into ResourceMaster, ensure you have the following installed:
- Python 3.7+
- Jupyter Notebook or JupyterLab
- Required Python packages:
  ```bash
  pip install gym==0.26.2 numpy stable-baselines3 shimmy>=2.0 matplotlib ipywidgets torch
  ```

### Installation
1. Clone the repository:
   
2. Install dependencies:
  
3. Open the Jupyter Notebook:
   ```bash
   jupyter notebook Project_4_RL_driven_Resource_Allocation_in_a_Simulated_Environment.ipynb
   ```

### Running the Simulation
1. **Launch the Notebook**: Open the `.ipynb` file in Jupyter.
2. **Train the Agent**: Run the cells to initialize the environment and train the PPO model (takes a few minutes).
3. **Interact with the Simulation**: Use the sliders to adjust:
   - **Task Arrival Probability (p)**: Controls how often new tasks arrive (0.1 to 1.0).
   - **CPU Capacity**: Resources allocated per step (1 to 5 units).
   - **Memory Capacity**: Memory allocated per step (1 to 5 units).
4. **Watch the Magic**: The simulation visualizes CPU and memory loads, task completions, and performance trends in real-time.

---

## 🎮 **How It Works**

### The Environment
The `AdvancedResourceAllocationEnv` is a custom Gym environment where:
- **State**: Represents CPU and memory loads across `N=5` slots.
- **Action**: The agent selects a slot (0 to 4) to allocate resources.
- **Reward**: Earns +1 for completing a task (when both CPU and memory reach 0).
- **Task Arrival**: New tasks arrive with probability `p`, randomly assigned to empty slots with CPU/memory demands up to `M=10`.
- **Termination**: Episodes end after `max_steps=1000` or when specified.

### The Agent
The PPO agent, trained with Stable-Baselines3, learns to prioritize slots with tasks, balancing resource allocation to maximize task completions. It uses a Multi-Layer Perceptron (MLP) policy and is optimized for GPU acceleration with PyTorch.

### Visualization
The interactive dashboard displays:
- **CPU and Memory Bar Charts**: Show current loads per slot, highlighting the agent's actions, new tasks, and completions.
- **Performance Trends**: Plot cumulative rewards, CPU, and memory usage over time.
- **Logs**: User-friendly messages detail the agent's decisions and task events.

---

## 🚧 **Challenges and Solutions**

- **Challenge**: Balancing exploration and exploitation in a dynamic environment.
  - **Solution**: PPO's clipped objective ensures stable learning, with 100,000 timesteps for robust policy development.
- **Challenge**: Visualizing complex state transitions.
  - **Solution**: Dual bar charts and trend plots provide intuitive insights, with color-coded annotations for clarity.
- **Challenge**: Resource constraints on different hardware.
  - **Solution**: Automatic detection of CUDA for GPU training, with CPU fallback for broader compatibility.

---

## 🌍 **Real-World Applications**

ResourceMaster isn't just a simulation—it's a blueprint for real-world systems:
- **Cloud Computing**: Optimize resource allocation in data centers.
- **Edge Computing**: Manage tasks in IoT devices with limited resources.
- **Task Scheduling**: Improve efficiency in multi-core processors or distributed systems.
- **AI-Driven Operations**: Apply RL to dynamic resource management in robotics or smart grids.

---

## 📈 **Performance Highlights**

After training, the agent achieves an average reward of **~224.5 ± 5.24** over 10 episodes, demonstrating robust task completion. The interactive simulation lets you tweak parameters to explore how the agent adapts to varying workloads.

---

## 🤝 **Contributing**

We welcome contributions to make ResourceMaster even better! Here’s how you can help:
1. Fork the repository.
2. Create a feature branch (`git checkout -b feature/amazing-feature`).
3. Commit your changes (`git commit -m 'Add amazing feature'`).
4. Push to the branch (`git push origin feature/amazing-feature`).
5. Open a Pull Request.

Ideas for contributions:
- Enhance the environment with new resource types (e.g., bandwidth).
- Add support for other RL algorithms (e.g., DQN, A2C).
- Improve visualization with 3D plots or animations.
- Optimize hyperparameters for better performance.

---

## 📚 **Resources**

- **Stable-Baselines3**: [Documentation](https://stable-baselines3.readthedocs.io/)
- **Gym**: [Documentation](https://www.gymlibrary.dev/)
- **PyTorch**: [Documentation](https://pytorch.org/docs/stable/index.html)
- **Matplotlib**: [Documentation](https://matplotlib.org/stable/contents.html)
- **Jupyter Widgets**: [Documentation](https://ipywidgets.readthedocs.io/)

---

## 🌟 **Why ResourceMaster?**

ResourceMaster stands out by blending cutting-edge RL with an engaging, interactive interface. It’s not just about code—it’s about understanding how intelligent systems can adapt to dynamic challenges. Whether you're a student, researcher, or developer, this project offers a hands-on way to explore RL, resource management, and visualization.

**Ready to master resources with AI?** Clone the repo, fire up the notebook, and watch the agent optimize in real-time! 🚀

---

**License**: MIT  
**Author**: Myron Correia 
