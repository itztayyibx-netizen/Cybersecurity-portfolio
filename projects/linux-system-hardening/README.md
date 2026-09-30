# Linux System Hardening & Integrity Protection Lab

## Overview

This project documents practical Linux system hardening techniques performed within an authorised university cybersecurity laboratory environment.

The exercises involved applying defensive security controls to protect files, system logs, configuration directories, and shell access against simulated attacks.

The purpose of the project was to understand how Linux permissions, file attributes, and filesystem controls can be used to reduce unauthorised modification and improve system integrity.

## Scope

All activities were performed within an authorised university cybersecurity laboratory environment using simulated attacks provided as part of the lab exercises.

No unauthorised or public systems were targeted.

## Tools and Technologies

- Linux
- Linux command line
- chmod
- chattr
- lsattr
- mount
- findmnt

## Methodology

The exercises followed a defensive security process:

1. Identify the resource targeted by the simulated attack.
2. Determine an appropriate Linux security control.
3. Apply the security control using the command line.
4. Verify that the configuration was applied.
5. Allow the simulated attack to execute.
6. Confirm whether the security control prevented the intended action.
7. Record evidence of the result.

# Security Controls

## 1. File Permission Protection

Linux file permissions were configured to prevent another user from modifying a protected file.

The simulated attack attempted to write to the file but was denied permission, demonstrating how appropriate file permissions can restrict unauthorised modification.

## 2. Immutable Log File Protection

The immutable file attribute was applied to a log file using `chattr +i`.

The configured attribute prevented the protected file from being deleted during the simulated attack.

This demonstrated how Linux file attributes can provide an additional layer of protection for important files.

## 3. Append-Only Log Protection

The log file was configured with the append-only attribute using `chattr +a`.

This allowed new information to be appended while preventing existing log content from being overwritten.

The exercise demonstrated how append-only controls can help protect the integrity of log data.

## 4. Read-Only System Configuration Protection

Filesystem controls were used to make the `/etc` directory read-only during the laboratory exercise.

The simulated attack attempted to create or modify system configuration data but failed because the filesystem was read-only.

This demonstrated how restricting write access to sensitive system locations can reduce the ability of an attacker to make unauthorised configuration changes.

## 5. Shell Execution Restriction

Execute permissions were removed from `/bin/bash` as part of the controlled laboratory exercise.

The simulated attack subsequently failed to obtain shell access.

This was an educational demonstration of Linux execution permissions rather than a recommended production configuration, as disabling shell execution could significantly affect legitimate system operation.

# Security Impact

Weak file permissions and insufficient protection of important system files can allow unauthorised users or processes to modify logs, alter configuration data, or interfere with system operation.

The exercises demonstrated how Linux permissions, file attributes, and filesystem restrictions can be used to limit these actions.

# Defensive Considerations

Potential defensive measures include:

- Apply least-privilege file and directory permissions.
- Restrict modification of sensitive system files.
- Protect important logs from unauthorised deletion or modification.
- Monitor changes to critical files and directories.
- Limit privileged access to trusted administrators.
- Regularly review filesystem permissions and security configurations.

# Skills Demonstrated

- Linux system security
- System hardening
- Linux file permissions
- File integrity protection
- Immutable file attributes
- Append-only logging
- Filesystem access control
- Command-line administration
- Security control validation
- Defensive cybersecurity
- Evidence documentation

# Limitations

The controls demonstrated in this project were implemented within a controlled educational laboratory.

Some techniques were intentionally used to demonstrate specific Linux security concepts and may not represent appropriate production configurations. Production hardening should consider system availability, operational requirements, access-control policies, monitoring, and established security baselines.

# Evidence

Selected screenshots from the authorised laboratory exercises demonstrate the configuration and validation of the Linux security controls.

# Ethical Considerations

All activities documented in this project were performed within an authorised cybersecurity laboratory environment designed for security education and testing.

The techniques were used solely for educational and defensive cybersecurity purposes.

# Conclusion

This project demonstrated practical Linux system-hardening techniques for protecting files, logs, system configuration, and shell access against simulated attacks.

The exercises provided hands-on experience with Linux permissions, file attributes, filesystem restrictions, security-control validation, and defensive system administration.
