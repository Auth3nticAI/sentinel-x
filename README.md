# Sentinel-X

Sentinel-X is a secure, GPS-denied autonomous reconnaissance software stack that combines ROS 2 middleware, visual-inertial localization, edge AI perception, and agentic mission control with a zero-trust security posture.

The goal of Sentinel-X is to demonstrate production-grade autonomy under real constraints:
- no GPS assumptions
- intermittent connectivity
- edge compute limits
- secure communications
- human-on-the-loop oversight
- measurable performance and failure handling

## Why this project exists

Modern autonomous systems in defense and safety-critical environments must operate without reliable GPS and cannot depend on continuous teleoperation. Sentinel-X focuses on the systems integration gap that most student projects avoid:
- localization and navigation in degraded conditions
- low-latency perception on edge hardware
- secure ROS 2 communication graphs (SROS2 / DDS security)
- mission intent translated into constrained actions
- logging and post-mission auditability

## Core capabilities

- **GPS-denied localization:** visual-inertial SLAM for pose estimation and mapping  
- **Autonomy and navigation:** path planning + execution using ROS 2 navigation components  
- **Edge AI perception:** object detection / segmentation pipelines with performance profiling  
- **Agentic mission layer:** intent-to-action interface with tool constraints and safety boundaries  
- **Zero-trust posture:** authenticated nodes, encrypted transport, command injection resistance  
- **Operational logging:** metrics, telemetry, and audit trails for performance evaluation

## Architecture (high level)

Sentinel-X is structured as layered autonomy:

1. **Edge Node (ROS 2)**
   - sensor ingestion (camera, IMU)
   - localization + mapping
   - perception inference
   - command execution + local logging

2. **Autonomy Stack**
   - planning, navigation, obstacle handling
   - mission constraints and state machine
   - fault detection and recovery

3. **Operator Oversight**
   - human approval and override controls
   - telemetry visualization (optional)
   - post-mission review via logs and metrics

See `docs/architecture.md` for details.

## Repo structure

- `ros2_ws/` ROS 2 workspace and packages
- `docker/` containerized dev environment
- `notebooks/` ML and vision math foundations and experiments
- `docs/` architecture notes, metrics, diagrams
- `scripts/` helper scripts

## Getting started (dev environment)

### Prerequisites
- Docker Desktop
- Git

### Run ROS 2 Humble container
1. Build and start:
   - `docker compose up --build`
2. Open a shell inside the container:
   - `docker exec -it <container_name> bash`
3. Verify ROS:
   - `ros2 --help`

## Week 1 milestone

Week 1 is focused on environment + fundamentals:
- ROS 2 Humble running in Docker
- repo structure + documentation baseline
- linear regression from scratch with loss curve plot
- image array representation drills

See:
- `notebooks/01_linear_regression_from_scratch.ipynb`

## Roadmap

- Term 1: perception foundation + ML fundamentals + cloud baseline
- Term 2: GPS-denied localization + planning algorithms + security basics
- Term 3: ROS 2 mastery + mission intent layer
- Term 4: DevOps + networking + embedded realism
- Term 5: PyTorch deep learning + secure SWE + telemetry storage
- Term 6: agentic autonomy + AI security evaluation + final integration demo

## License
MIT (or choose later)
