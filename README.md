# X-Repo2Run

An LLM-based build agent system that helps manage and automate build processes in containerized environments in various programming languages. This project provides tools for handling dependencies, resolving conflicts, and managing build configurations.

## Features

- Docker-based sandbox environment for isolated builds
- Automated dependency management and conflict resolution
- Waiting list and conflict list management for package dependencies
- Error format handling and output collection

## Prerequisites

- Python 3.x
- Docker
- Git

## Installation

1. Clone the repository:
```bash
git clone https://github.com/terryyz/x-repo2run
cd x-repo2run
```

2. Install the required dependencies:
```bash
pip install -r requirements.txt
```

## Usage

Move tools `tools` to `/home/tools`.

The main entry point is through the build agent's main script. You can run it with the following arguments:

```bash
python build_agent/main.py <repository_full_name> <sha>
```

Where:
- `repository_full_name`: The full name of the repository (e.g., user/repo)
- `sha`: The commit SHA
- `root_path`: The root path for the build process

## Project Structure

- `build_agent/` - Main package directory
  - `agents/` - Agent implementations for build configuration
  - `utils/` - Utility functions and helper classes
  - `docker/` - Docker-related configurations
  - `main.py` - Main entry point
  - `multi_main.py` - Multi-process support

## Features in Detail

### Sandbox Environment
The project uses Docker containers to create isolated build environments, ensuring clean and reproducible builds.

### Dependency Management
- **Waiting List**: Manages package installation queue
- **Conflict Resolution**: Handles version conflicts between packages
- **Error Handling**: Formats and processes build errors

### Configuration Agent
Utilizes GPT models to assist in build configuration and problem resolution.

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## Citation

```bibtex
@article{zhuo2025config,
  title={Configuraing Multilingual Docker Environment via Code Agent},
  author={Zhuo, Terry Yue},
  year={2025}
}
```

## License

Apache-2.0

## Ackowledgement

- [https://github.com/bytedance/Repo2Run](https://github.com/bytedance/Repo2Run)
- [https://github.com/Aider-AI/aider](https://github.com/Aider-AI/aider)


## Contact

terry.zhuo@moansh.edu
