# Class Creator

Automate the creation of C++ class files and a Makefile for your C++ programs with this Bash script.
All created classes are in form of the orthodox canonical form:

Example for user_input:
```ruby

   ________                    ______                __
  / ____/ /___ ___________    / ____/_______  ____ _/ /_____  _____
 / /   / / __ / __/ __ \/ ___/
/ /___/ / /_/ (__  |__  )   / /___/ /  /  __/ /_/ / /_/ /_/ / /
\____/_/\__,_/____/____/____\____/_/   \___/\__,_/\__/\____/_/
                      /_____/

Script completed successfully.
Enter the class name without .hpp (or 'done' to finish): Example
Enter the class name without .hpp (or 'done' to finish): done
You entered the following class names:
Example
```

Created hpp-file:
```
#ifndef EXAMPLE_HPP
#define EXAMPLE_HPP

#include <string>
#include <iostream>

class example
{
private:
	// Class members

public:
	example();
	example(std::string type);
	example(const example &other);
	~example();
	example &operator=(const example &other);
};

#endif
```
Created cpp functions in Example.cpp:
```ruby
#include "Header.h"
#include "Example.hpp"

// Implement class methods here

Example::Example()
{
	std::cout << "Example default constructor called" << std::endl;
}

Example::Example(std::string type)
{
	std::cout << "Example constructor with type called" << std::endl;
}

Example::Example(const Example &other)
{
	*this = other;
	std::cout << "Example copy constructor called" << std::endl;
}

Example::~Example()
{
	std::cout << "Example destructor called" << std::endl;
}

Example &Example::operator=(const Example &other)
{
	if (this == &other)
		return *this;
	std::cout << "Example copy assignment constructor called" << std::endl;
	return *this;
}
```


## Features

- Easily create C++ class files with customizable class names.
- Generates header files (`*.hpp`) and source files (`*.cpp`) with placeholder methods.
- Includes a pre-configured `Makefile` and `main.cpp` for compiling your C++ program.
- Provides a simple, guided interface for adding class names.

## Getting Started

1. Clone this repository to your local machine:

```bash
git clone https://github.com/your-username/your-repo.git
```
Navigate to the project directory:
```
cd your-repo
```
Make the script executable:
```
chmod +x class_creator.sh
```

Run the script:
```
./class_creator.sh
```

Follow the on-screen instructions to create your C++ class files and Makefile.

Usage
When prompted, enter the desired class names without the .hpp extension.
The script will generate corresponding .hpp and .cpp files for each class.
Edit the generated files as needed to implement your class functionality.
Run make to compile your program using the generated Makefile.
Contributing
Contributions are welcome! Feel free to open issues or submit pull requests.
