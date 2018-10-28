# citygml-tools
citygml-tools is a CLI program that bundles several operations for processing
CityGML files.

## License
citygml-tools is licensed under the [Apache License, Version 2.0](http://www.apache.org/licenses/LICENSE-2.0). See the `LICENSE` file for more details.

## Latest release
The latest stable release of citygml-tools is 0.5.

Download the citygml-tools 0.5 release binaries [here](https://github.com/citygml4j/citygml-tools/releases/download/v0.5/citygml-tools-0.5.zip). Previous releases are available from the [releases section](https://github.com/citygml4j/citygml-tools/releases).

## Contributing
* To file bugs found in the software create a GitHub issue.
* To contribute code for fixing filed issues create a pull request with the issue id.
* To propose a new feature create a GitHub issue and open a discussion.

## How to use citygml-tools
Download and unzip the latest release or build the program from source. Afterwards, open a shell environment and execute the `citygml-tools` script from the `bin` folder to launch the program.

Use the following command to list the available operations.

    > citygml-tools --help
    
    Usage: citygml-tools [-hV] [--log=<logLevel>] [COMMAND]
    Collection of tools for processing CityGML files.
          --log=<logLevel>   Log level: debug, info, warn, error (default: info).
      -h, --help             Show this help message and exit.
      -V, --version          Print version information and exit.
    Commands:
      help              Displays help information about the specified command
      move-global-apps  Converts global appearances to local ones.
      clip-textures     Clips texture images to the extent of the target surface.
      from-cityjson     Converts CityJSON files into CityGML.
      to-cityjson       Converts CityGML files into CityJSON.

To display information about how to use a specific command, type the
following:

    > citygml-tools help [COMMAND]

## Building
citygml-tools uses [Gradle](https://gradle.org/) as build system. To build the program from source, clone the repository to your local machine and run the following command from the root of the repository. 

    > gradlew installDist
    
The script automatically downloads all required dependencies for building and running citygml-tools. So make sure you are connected to the internet. The build process runs on all major operating systems and only requires a Java 8 JDK or higher to run.

If the build was successful, you will find the citygml-tools package under `citygml-tools/build/install`.