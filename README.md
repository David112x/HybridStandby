# Hybrid Standby
## This is a concept that is currently in development.

Hybrid Standby, a service for Windows that aims to improve S0/Modern Standby/Low Power Idle, it does this by listening for power events and checking in on the CPU's states (C-states), when the system enters S0 Low Power Idle, it will suspend non-critical system applications and services and when leaving modern standby (waking up), it wakes up all of those processes so that the system may resume working as intended.

There is still research to be done for this, so the idea isn't fully fledged out.

## Things that are planned:
- Disable Low Power Idle Network Connected while using HybridStandby (no reason to have this if the system isn't going to do anything with it, not even Windows Updates).

While not all of the cons of S0/Low Power Idle can be taken out by improving it since the concept of Modern Standby is flawed in some ways, the others can still be adjusted and accounted for.

## Notes
- Develop the kernel-mode component, this component notifies the user-mode component when the CPU is entering a C-state like C6 (on all cores) and the user-mode component takes this into account if it has already been notified by Windows itself that the system is entering a suspend state.
- Release sources once the kernel-mode component is finished.