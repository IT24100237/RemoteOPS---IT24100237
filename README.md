# IE3090 RemoteOps

## Student Information

Registration Number: IT24100237

## Project Description

RemoteOps is a remote system monitoring and management application developed
in C using TCP/IP and UDP socket programming for the IE3090 Network
Programming assignment.

The system consists of an Agent and a Controller. The Controller connects to
the Agent through TCP to perform authenticated remote operations. UDP is used
separately for periodic system monitoring.

## Personalised Values

- Agent TCP Port: 9410
- Session ID: SID:7320
- Authentication Token: OPS-0237
- Agent Source: agent_237.c
- Controller Source: controller_237.c
- Makefile: Makefile_237
- Log File: remoteops_IT24100237.log
- Storage Path: ./agentfiles/IT24100237/

## Main Features

- TCP Agent/Controller communication
- Authentication using personalised token
- Multiple Controller support using POSIX threads
- SYSINFO system information
- LISTPROC process listing
- Restricted EXEC commands
- PUT file upload
- GET file download
- UDP system monitoring
- Error handling
- Activity logging
- Graceful QUIT operation

## Compilation

To clean previous builds:

make -f Makefile_237 clean

To compile the project:

make -f Makefile_237

This creates:

agent_237
controller_237

## Running the Agent

Open a terminal and run:

./agent_237

The Agent listens for TCP connections on port 7320.

## Running the Controller

Open another terminal in the same project directory and run:

./controller_237

## Authentication

After connecting, authenticate using:

AUTH OPS-0237

## Supported Commands

SYSINFO

LISTPROC

EXEC DATE

EXEC UPTIME

EXEC HOSTNAME

PUT <filename>

GET <filename>

MONITOR START 9510

MONITOR STOP

QUIT

## EXEC Restrictions

Only the following EXEC commands are permitted:

- DATE
- UPTIME
- HOSTNAME

Other EXEC commands are rejected.

## File Storage

Files uploaded using PUT are stored inside:

./agentfiles/IT24100237/

## Activity Log

Agent activities are recorded in:

remoteops_IT24100237.log

## Notes

The project was developed and tested in a CentOS Linux environment.

Git and GitHub were used during development to maintain the project history.
