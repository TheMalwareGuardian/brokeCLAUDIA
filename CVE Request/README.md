## Submit a CVE Request

### Url

- https://cveform.mitre.org/

### Select a request type

- Report Vulnerability/Request CVE ID

### Enter your e-mail address

- @

### Number of vulnerabilities reported or IDs requested (1-10)

- 1

### Vulnerability type

- Incorrect Access Control

### Vendor of the product(s)

- National Cryptologic Centre (CCN-CERT - CNI), Spain

### Affected product(s)/code base

- microCLAUDIA
	- Versions 3.2.0 and earlier (fixed in 3.2.2)

### Attack type

- Remote

### Impact

- Information Disclosure
- Escalation of Privileges

### Affected component(s)

- Cross-organization access validation logic, central cloud service

### Attack vector(s)

- To exploit the vulnerability, an attacker must have access to a valid microCLAUDIA account. Once logged in to the central cloud service, if the attacker obtains identifiers belonging to another organization - for example, by reviewing browser history on a compromised endpoint or simply by guessing - they can craft direct API requests to perform unauthorized actions on systems outside of their assigned organization. These actions may include listing assets with the agent installed, uninstalling the agent, deleting configured vaccines, and more.

### Suggested description of the vulnerability for use in the CVE

- microCLAUDIA through version 3.2.0 contains a broken access control vulnerability in its central cloud service. An authenticated user can perform unauthorized actions on systems belonging to other organizations by crafting direct API requests using organization identifiers obtained from a compromised endpoint or guessed manually. This allows cross-tenant access, enabling the attacker to list and manage remote assets, uninstall agents, and delete vaccine configurations. The issue was addressed in version 3.2.2.

### Discoverer(s)/Credits

- Alejandro Vazquez Vazquez

### Reference(s)

- https://github.com/TheMalwareGuardian/brokeCLAUDIA

### Additional information

- First report sent to incidentes@ccn-cert.cni.es on March 11, 2024.
- Vulnerability independently validated on versions 2.16.3 and 3.2.0.
- Issue confirmed resolved in version 3.2.2. As of version 3.6.1, the vulnerability remains fully patched.
- A responsible disclosure period has been respected before publishing public details.
- The referenced public GitHub repository includes the exploitation tool, a video demo with blurred sensitive information, and the email exchange with CCN-CERT where they acknowledged the report and thanked the researcher for assisting in the resolution.
