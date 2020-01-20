## vctl exec container

Execute a command within a running container.

### Synopsis

Run the given command within the specified container.
* If the COMMAND to execute has any flags in common [e.g. -t], two dashes '--' must be used to separate the COMMAND's flags/arguments.

```
vctl exec container CONTAINER [options] -- COMMAND [arguments...]
```

### Examples

```
  # To get output from running 'date' command in myContainer.
  vctl exec container myContainer date
  # To list contents of myContainer and sort by the modification time. ['--' must be used here to seperate '-t'].
  vctl exec container myContainer -- ls -t
```

### Options

```
  -d, --detach           Detach from the task once the execution starts
      --exec-id string   Exec specific ID for the process
  -h, --help             help for container
  -t, --tty              Allocate a tty for the container
```

### SEE ALSO

* [vctl exec](vctl_exec.md)	 - Execute a command within containers or virtual machines.

###### Auto generated by spf13/cobra on 16-Jan-2020