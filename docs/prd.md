Autonomous Concrete Pouring System (V1)

1. Problem
Fill a defined target region (e.g. pothole) with material evenly using an autonomous nozzle.

2. System
- 2D grid workspace
- target region (mask)
- nozzle (position + flow rate + pouring state)
- material deposition process

3. State (Inputs)
- current fill map (grid of deposited material)
- target mask (desired fill region)
- nozzle position (x, y)
- current flow rate
- pouring state (on/off)

4. Actions (Outputs)
- move nozzle (dx, dy)
- adjust flow rate (dflow)
- toggle pouring (on/off)

5. Objective
Minimize:
- underfill (missing material inside target)
- overfill (excess material inside target)
- waste (material outside target)
- time (number of steps)

6. Constraints
- grid-based simulation (no continuous physics)
- discrete time steps
- fixed workspace boundaries
- simplified deposition model (no real fluid dynamics)
- static environment (no moving terrain or obstacles)

7. Success Criteria
- ≥ X% of target region filled within tolerance
- ≤ Y total waste outside target
- ≤ Z total overfill inside target
- completes in ≤ N steps
