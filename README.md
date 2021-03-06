# terminal-spawner
This is a shell script that can be used to run a command in a new macOS terminal.

This tool is useful for chaining commands, involving some blocking commands that take control of the terminal, but need to occur before some other command. 

For example starting up metro-bundler before building and running a React Native application on iOS.

# Usage
## Basic
Run command in a new terminal in the current directory

eg. `./spawn-terminal-with-command.sh "npm start"`

## With Location
Use `-l` or `--location` to specify location to run new command in

eg. `./spawn-terminal-with-command.sh -l ~/Documents/AwesomeProject "npm start"`

## Chaining Commands
You may chain a blocking command like this:

`./spawn-terminal-with-command.sh "npm start"; npx react-native run-ios`

## Help
Use `-h` or `--help` flag to get help

`./spawn-terminal-with-command.sh -h`
