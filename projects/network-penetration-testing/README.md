# Network Penetration Testing Lab

## Overview

This project documents practical network penetration testing performed within an authorised cybersecurity laboratory environment.

The assessment involved network reconnaissance, port and service enumeration, vulnerability identification, and controlled exploitation using Nmap and the Metasploit Framework.

The purpose of the project was to develop a structured understanding of how network services can be discovered, assessed, and tested for known security weaknesses.

## Scope

All testing was performed within authorised university cybersecurity laboratory environments using systems provided for security testing.

No unauthorised or public systems were targeted.

## Tools Used

- Kali Linux
- Nmap
- Metasploit Framework
- MSFconsole

## Methodology

The testing process followed a structured penetration-testing workflow:

1. Identify the target system within the authorised lab environment.
2. Perform network reconnaissance.
3. Scan TCP ports using Nmap.
4. Enumerate exposed services and service versions.
5. Review discovered services for potential vulnerabilities.
6. Select an appropriate Metasploit module for a vulnerable service.
7. Configure the exploit against the authorised target.
8. Perform controlled exploitation.
9. Record evidence of the testing process.
10. Consider appropriate mitigation measures.

# Findings

## Finding 1 – Network Reconnaissance and Service Enumeration

Nmap was used to perform network reconnaissance against the authorised laboratory target.

A full port and service scan was performed to identify exposed ports and determine the services operating on the target system.

The results demonstrated how port scanning and service enumeration can be used during the reconnaissance stage of a penetration test to identify potential attack surfaces.

## Finding 2 – UnrealIRCd Service Exploitation

Service enumeration identified an UnrealIRCd service within the controlled laboratory environment.

The Metasploit Framework was used to investigate the service and configure the `unix/irc/unreal_ircd_3281_backdoor` exploit module.

The relevant target information and exploit options were configured within MSFconsole before the exploit was executed against the authorised laboratory system.

This exercise demonstrated how information discovered during reconnaissance can be used to investigate and validate a known vulnerability within a controlled environment.

## Security Impact

A vulnerable network-facing service can provide an attacker with an opportunity to gain unauthorised access to a system.

This demonstrates the importance of maintaining supported software versions, applying security updates, limiting unnecessary network exposure, and regularly assessing externally accessible services.

## Mitigation

Potential defensive measures include:

- Remove or disable unnecessary network services.
- Keep network-facing software patched and supported.
- Restrict access to sensitive services using firewall rules.
- Regularly scan systems for exposed and outdated services.
- Monitor network activity for suspicious connections and exploitation attempts.

# Skills Demonstrated

- Network reconnaissance
- Port scanning
- Service enumeration
- Vulnerability identification
- Nmap
- Kali Linux
- Metasploit Framework
- MSFconsole
- Controlled exploitation
- Security remediation
- Evidence documentation

# Evidence

Selected screenshots from the authorised laboratory exercises demonstrate the Nmap reconnaissance and controlled Metasploit exploitation process.

# Ethical Considerations

All penetration-testing activity documented in this project was performed within authorised cybersecurity laboratory environments designed for security testing.

The techniques documented here were used solely for educational and defensive cybersecurity purposes.

# Conclusion

This project demonstrated a structured network penetration-testing process from reconnaissance and service enumeration through to vulnerability investigation and controlled exploitation.

Using Nmap and the Metasploit Framework provided practical experience in identifying exposed network services, investigating potential vulnerabilities, validating a known security weakness in an authorised environment, and considering appropriate mitigation measures.
