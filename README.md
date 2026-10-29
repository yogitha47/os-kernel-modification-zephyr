# OS Mini Project: Modifying a Small OS Kernel

## Project Overview
This project demonstrates a kernel-level modification in Zephyr RTOS
by adding diagnostic messages to thread-switch tracing hooks.

## Operating System
- Zephyr RTOS
- Target: qemu_x86 / atom
- Emulator: QEMU
- Environment: Ubuntu 24.04 on WSL2

## Kernel Modification
The file `source/tracing_user.c` contains implementations of:
- `sys_trace_thread_switched_in_user()`
- `sys_trace_thread_switched_out_user()`

The hooks print diagnostic messages using `printk()`.

## Configuration
The `modified.conf` file enables:
- `CONFIG_TRACING=y`
- `CONFIG_TRACING_USER=y`

## Evidence
The file `evidence/modified_run.log` contains output from the modified
Zephyr build running in QEMU.

## Team Members
- Yogitha Malasani
- Shivangi Kesarwani
