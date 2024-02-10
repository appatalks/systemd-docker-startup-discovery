# Startup Discovery Script

This script is designed to list and analyze the startup sequence of system services and Docker containers on ```systemd``` based systems. It provides insights into the startup duration, order, and start timestamp of each service and Docker container since the last boot. This can be useful for system administrators and developers looking to optimize startup times and understand service dependencies.

## Features

- Generates a detailed log file with timestamps, duration, and order of system service startups.
- Identifies Docker containers' startup details if Docker is installed and running.
- Outputs logs to a file with a dynamic name based on the current date and time.

## Prerequisites

- Requires `sudo` privileges for execution.
- Docker (optional): To log startup details of Docker containers.

## Usage

1. Download the script `startup_discovery.sh` to your local machine.
2. Make the script executable:
   ```bash
   chmod +x startup_discovery.sh
   ```
3. Run the script with sudo to ensure it has the necessary permissions:
   ```bash
   sudo /bin/bash startup_discovery.sh
   ```

## Log File

After execution, the script generates a log file in the `/var/log` directory. The file name is `service_and_docker_startup_details_<YYYY-MM-DD_HH-MM-SS>.log`, where the date and time reflect when the script was run. The log file includes:

- System service startup durations, order, and timestamps.
- Docker containers startup details, including start time and container names, if applicable.

## Contributing

Feel free to fork this project and submit pull requests for improvements or bug fixes. For major changes, please open an issue first to discuss what you would like to change.
