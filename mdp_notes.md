# Vacuum MDP Environment

## Environment
- Grid size: 4 columns by 4 rows
- Agent: vacuum robot
- State: robot coordinate position
- Obstacle: cell marked by 'X', cannot be entered
- Terminal States: -1 and 10

## Actions
- Up
- Down
- Left
- Right

## Transition model
- 80% chance of moving in intended direction (go North)
- 10% chance of moving leftmost of the intended direction (go West)
- 10% chance of moving rightmost of the intended direction (go East)
- if movement results in colliding with an obstacle or wall, agent remains in current position

## Reward model
- Living costs: -0.05, -2, 2
- Terminal costs: -1, 10

## Agent
- Type: MDP-based vacuum agent
- Discount Factor: 0.9
- Uses AIMA's GridMDP
- Continues selecting actions until reaching terminal state or exhausting moves
- Max actions: 15