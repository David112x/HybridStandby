# HybridStandby
## This is currently a concept that is in developed, no actual program has been developed or has entered development yet.

Hybrid Standby, a service for Windows that aims to improve S0/Modern Standby/Low Power Idle, it does this by listening for power events and in the case of the system entering modern standby, it will suspend non-critical system applications and services and when leaving modern standby (waking up), it wakes up all of those processes so that the system may resume working normally.

There is still research to be done for this, so the idea isn't fully fledged out.

## Things to reseach:
- What "Turn off hard disk after" does in Windows in systems with S0/Low Power Idle.
- If user applications do get suspended instead of being allowed to run in the background while in S0/Low Power Idle.

## Things that are planned:
- Disable Low Power Idle Network Connected while using HybridStandby (no reason to have this if the system isn't going to do anything with it, not even Windows Updates).

While not all of the cons of S0/Low Power Idle can be taken out by improving it since the concept of Modern Standby is flawed in some ways, the others can still be adjusted and accounted for.
