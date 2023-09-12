# Class Creator

Automate the creation of C++ class files and a Makefile for your C++ programs with this Bash script.

## Features

- Easily create C++ class files with customizable class names.
- Generates header files (`*.hpp`) and source files (`*.cpp`) with placeholder methods.
- Includes a pre-configured `Makefile` and `main.cpp` for compiling your C++ program.
- Provides a simple, guided interface for adding class names.

## Getting Started

1. Clone this repository to your local machine:

   ```bash
   git clone https://github.com/your-username/your-repo.git
Navigate to the project directory:

cd your-repo
Make the script executable:

chmod +x class_creator.sh

Run the script:
./class_creator.sh

Follow the on-screen instructions to create your C++ class files and Makefile.

Usage
When prompted, enter the desired class names without the .hpp extension.
The script will generate corresponding .hpp and .cpp files for each class.
Edit the generated files as needed to implement your class functionality.
Run make to compile your program using the generated Makefile.
Contributing
Contributions are welcome! Feel free to open issues or submit pull requests.


```bash
# Your Bash code here

```bash
#!/bin/bash

# Initialize arrays for class names and source files
class_names=()
source_files=()

# ... (rest of your script here)

echo "You entered the following class names:"
for class_name in "${class_names[@]}"; do
    echo "$class_name"
done
