# LibTorch AMD64 Build

## Overview
This repository provides a custom-built LibTorch library for AMD64 architecture. PyTorch does not officially provide pre-built LibTorch binaries for AMD64, making this build particularly valuable for developers targeting this architecture. This project aims to fill that gap by offering a ready-to-use LibTorch AMD64 build for machine learning and deep learning applications.

## Features
- **Custom AMD64 Build**: A fully functional LibTorch build tailored for AMD64 systems.
- **Compatibility**: Compatible with standard PyTorch workflows and C++ applications.
- **Optimized Performance**: Built to leverage AMD64 architecture for efficient computation.

## Installation
1. **Download the Build**:
   - Clone this repository:
     ```bash
     git clone https://github.com/kamisaberi/libtorch-amd64-build.git
     ```
2. **Set Up Your Environment**:
   - Ensure you have the necessary dependencies installed (e.g., CMake, C++ compiler).
   - Extract the downloaded LibTorch archive to your project directory.

3. **Link in Your Project**:
   - Update your project's CMakeLists.txt to include the LibTorch library:
     ```cmake
     find_package(Torch REQUIRED)
     target_link_libraries(your_project_name "${TORCH_LIBRARIES}")
     ```
   - Refer to the [PyTorch C++ API documentation](https://pytorch.org/cppdocs/) for detailed usage.

## Build Details
PyTorch officially supports LibTorch builds for specific architectures, but AMD64 is not included in their pre-built binaries. This repository provides a custom LibTorch build for AMD64, compiled from source with the following specifications:
- **LibTorch Version**: [Specify the version, e.g., 2.3.0]
- **Architecture**: AMD64
- **Build Environment**: [Specify OS, e.g., Ubuntu 20.04, and compiler, e.g., GCC 9.3]
- **Optimizations**: [Mention any specific optimizations, e.g., CPU-specific flags, if applicable]

The build process involved [briefly describe key steps, e.g., configuring CMake, setting architecture flags, resolving dependencies]. This ensures compatibility and performance on AMD64 systems.

## Usage Example
Here’s a simple C++ example using the LibTorch AMD64 build:

```cpp
#include <torch/torch.h>
#include <iostream>

int main() {
    torch::Tensor tensor = torch::rand({2, 3});
    std::cout << tensor << std::endl;
    return 0;
}
```

Compile and run the example with:
```bash
mkdir build && cd build
cmake -DCMAKE_PREFIX_PATH=/path/to/libtorch ..
make
./your_executable
```

## Contributing
Contributions are welcome! If you encounter issues or want to improve the build, please:
1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Make your changes and commit (`git commit -m "Add feature"`).
4. Push to the branch (`git push origin feature-branch`).
5. Open a Pull Request.

Please ensure your changes are tested on AMD64 systems.

## Issues and Support
If you face any issues or have questions, please open an issue on this repository. Provide details such as your OS, compiler version, and any error messages.

## License
This project is licensed under the [MIT License](LICENSE). The LibTorch library is subject to the [PyTorch License](https://github.com/pytorch/pytorch/blob/main/LICENSE).

## Acknowledgments
- Thanks to the PyTorch community for their excellent documentation and support.
- Built with ❤️ for the AMD64 community.
