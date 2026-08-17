# Linux Kernel Module & Driver Experiments

A collection of small educational Linux kernel-module experiments written
in C.

These experiments were created in 2019 while studying Linux kernel
programming and basic driver concepts. They are intentionally small and
focus on learning kernel APIs and mechanisms rather than implementing
production-ready drivers.

## Experiments

### `driver_file_operations`

A simple kernel module exploring file-operation callbacks and interaction
between user space and a kernel module.

Topics include:

- Kernel module initialization and cleanup
- File operations
- Character-device concepts
- Communication between user space and kernel space

### `driver_linked_list`

An experiment with linked lists provided by the Linux kernel.

Topics include:

- `struct list_head`
- Adding and removing entries
- Traversing kernel linked lists
- Kernel memory management

### `driver_params_kobject`

Explores module parameters and kernel objects.

Topics include:

- Kernel module parameters
- `kobject`
- Exposing module information through the kernel object model

### `driver_timer`

A small experiment with kernel timers.

Topics include:

- Kernel timers
- Timer callbacks
- Scheduling deferred work from a kernel module

### `driver_with_dynamic_node`

An experiment with dynamically created device nodes.

Topics include:

- Character devices
- Dynamic device numbers
- Device registration
- Device nodes
- User-space interaction with a kernel module

### `driver_with_ioctl`

A simple character-device experiment using `ioctl` for communication
between user space and the kernel module.

Topics include:

- Character devices
- `ioctl`
- Kernel/user-space interfaces
- Device operations

### `list_module_names`

An experiment exploring how loaded kernel modules can be enumerated.

Topics include:

- Kernel module structures
- Kernel linked lists
- Enumerating loaded modules

## Concepts Explored

These experiments provided hands-on experience with:

- Linux kernel modules
- Kernel module initialization and cleanup
- Character devices
- File operations
- `ioctl`
- Kernel linked lists
- Kernel timers
- Module parameters
- `kobject`
- Device registration
- Dynamic device nodes
- Kernel/user-space interfaces
- Kernel module enumeration
- C programming in kernel space

## Building

The individual experiments contain their own source files and build
configuration.

Build instructions are provided in the corresponding directory.

Typical kernel-module builds use the Linux kernel build system:

```bash
make
````

To remove build artifacts:

```bash
make clean
```

## Loading a Module

Kernel modules can generally be loaded with:

```bash
sudo insmod <module>.ko
```

and removed with:

```bash
sudo rmmod <module>
```

Depending on the experiment, additional setup may be required.

Check the individual directory before loading a module.

> **Warning:** Kernel modules execute in kernel space. These experiments
> were written for learning purposes and should be tested in an
> appropriate development environment rather than on a system where
> stability is important.

## Background

These experiments were written in 2019 while studying Linux kernel
programming.

The goal was to gain practical familiarity with the boundary between
user space and kernel space and to experiment with basic Linux kernel
APIs.

The implementations are small educational exercises and are not intended
to be production-quality drivers.
