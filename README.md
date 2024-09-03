## AIM:

To create a MDP (Markov Decision Process) for the chosen problem statement.

## PROBLEM STATEMENT:

Indoor plant watering scheduled system.

### Problem Description

To develop a reinforcement learning system to optimize the watering schedule for indoor plants to ensure they receive the optimal amount of water, maintaining plant health while minimizing water usage.

### State Space

The system considers several factors to decide when and how much to water the plants:

Soil Moisture Level: This shows how wet or dry the soil is (e.g., dry, moist, wet, waterlogged).
Time Since Last Watering: This records how long it's been since the plant was last watered (e.g., hours, days).
Plant Type: Different plants need different amounts of water (e.g., cactus, fern, orchid).
Temperature: The surrounding temperature can affect how quickly the soil dries out (e.g., degrees Celsius or Fahrenheit).
Humidity: The moisture in the air also impacts soil moisture (e.g., percentage).

### Sample State

Soil Moisture Level: Moist
Time Since Last Watering: 3 days
Plant Type: Fern
Temperature: 22°C
Humidity: 60%

### Action Space

The system has a few choices for what to do when it’s time to decide on watering:

Water the Plant: Choose how much water to give (e.g., Small, Medium, Large).
Do Not Water: Decide to skip watering this time.
Adjust Watering Frequency: Change how often the plant should be watered (e.g., water more or less often).

### Sample Action

Water the plant with a Medium amount.

### Reward Function

The system earns points (rewards) based on how well it keeps the soil at the right moisture level:

Goal Achievement: Points are given for getting the soil to the desired moisture level (e.g., wet).
Overwatering Penalty: If the system overwaters and risks harming the plant, it loses points.
Reward Calculation:
The total reward is calculated by subtracting any overwatering penalty from the points earned for reaching the moisture goal.

Formula:
Reward = Goal Achievement - Overwatering Penalty

### Graphical Representation

![WhatsApp Image 2024-09-03 at 17 26 02_c886e239](https://github.com/user-attachments/assets/c2b05fdd-5df8-4b05-ba81-9a8d80316259)

## PYTHON REPRESENTATION:

```
mdp = {
    0: {
        0: [(0.8, 1, 1, 0), (0.2, 2, 1, 0)],  
        1: [(0.8, 2, 1, 0), (0.2, 3, 0, 0)],  
        2: [(0.8, 3, 0, 0), (0.2, 4, 0, 0)],  
        3: [(0.8, 4, 0, 0), (0.2, 1, 0, 0)]   
    },
    1: {
        0: [(0.8, 1, 1, 1), (0.2, 2, 1, 1)],  
        1: [(0.8, 2, 1, 1), (0.2, 3, 0, 1)],  
        2: [(0.8, 3, 0, 1), (0.2, 4, 0, 1)],  
        3: [(0.8, 4, 0, 1), (0.2, 1, 0, 1)]   
    },
    2: {
        0: [(0.8, 1, 1, 1), (0.2, 2, 1, 1)],  
        1: [(0.8, 2, 1, 1), (0.2, 3, 0, 1)],  
        2: [(0.8, 3, 0, 1), (0.2, 4, 0, 1)],  
        3: [(0.8, 4, 0, 1), (0.2, 1, 0, 1)]   
    },
    3: {
        0: [(0.8, 1, 0, 0), (0.2, 2, 0, 0)],  
        1: [(0.8, 2, 0, 0), (0.2, 3, 0, 0)],  
        2: [(0.8, 3, 0, 0), (0.2, 4, 0, 0)],  
        3: [(0.8, 4, 0, 0), (0.2, 1, 0, 0)]   
    },
    4: {
        0: [(0.8, 1, 0, 0), (0.2, 2, 0, 0)],  
        1: [(0.8, 2, 0, 0), (0.2, 3, 0, 0)],  
        2: [(0.8, 3, 0, 0), (0.2, 4, 0, 0)],  
        3: [(0.8, 4, 0, 0), (0.2, 1, 0, 0)]   
    }
}

```

## OUTPUT:

![Screenshot 2024-09-03 195206](https://github.com/user-attachments/assets/c1ce4bd4-a20f-4446-9a77-13e731f5d967)

## RESULT:

Thus, the MDP for the problem statement using python is implemented successfully.

