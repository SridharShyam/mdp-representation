![WhatsApp Image 2024-09-03 at 17 26 02_522f457f](https://github.com/user-attachments/assets/983415cf-9fb8-49e9-8c5b-635a60006f75)# MDP REPRESENTATION

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

![WhatsApp Image 2024-08-28 at 15 54 52_24d22352](https://github.com/user-attachments/assets/b2d60e78-10bd-45cf-a460-859e65081b98)

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

![WhatsApp Image 2024-09-03 at 17 26 02_b2334069](https://github.com/user-attachments/assets/90650d57-3fc1-46fd-9a97-7099afb2d5c8)

## RESULT:

Thus, the MDP for the problem statement using python is implemented successfully.

