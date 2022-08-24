# STIX/MISP Security Playbook Object Conversion
 
**This repository provides a mapping table and a reference process that allows converting between STIX 2.1 Course of Action objects that make use of the [Security Playbook extension](https://github.com/fovea-research/stix2.1-coa-playbook-extension) and [MISP Security Playbook objects](https://github.com/MISP/misp-objects/blob/main/objects/security-playbook/definition.json).**

Machine-readable `security playbook` objects are used to manage, store, and share cybersecurity playbooks and orchestration workflows and can integrate with other machine-readable Cyber Threat Intelligence (CTI) objects to provide additional context and, consequently, support cybersecurity automation.
<p align="center">
  <img src="/misp-stix.png"/>
</p>


* Sharing cybersecurity playbooks using STIX 2.1 has been proposed, developed, and documented in the following GitHub repository
(https://github.com/fovea-research/stix2.1-coa-playbook-extension). In particular, the STIX 2.1 Extension Definition mechanism was used to extend the Course of Action SDO type to support including descriptive metadata about playbooks and "encapsulate" cybersecurity playbooks for sharing purposes.

* Sharing cybersecurity playbooks using MISP motivated the development of a security-playbook object and was made available in the official MISP Project GitHub
(https://github.com/MISP/misp-objects/blob/main/objects/security-playbook/definition.json).

This repository provides a mapping table that allows converting between `STIX 2.1 Course of Action objects that make use of the Security Playbook extension` and `MISP Security Playbook objects`. Specifically, the mapping table associates the properties that comprise a security playbook extension using the STIX 2.1 COA SDO and the attributes that comprise a MISP security playbook object. In addition we recommend implementers to follow the conversion process below to minimize losing information during the conversion process.

More information about the data types of the properties/attributes which their knowledge is necessitated to perform conversions from one standard to another can be found in the following repositories. 

- [STIX 2.1 Course of Action - Security Playbook extension](https://github.com/fovea-research/stix2.1-coa-playbook-extension)
- [MISP Security Playbook object template](https://github.com/MISP/misp-objects/blob/main/objects/security-playbook/definition.json)

We understand that their inclusion in the table below would help engineers to codify it faster, but it creates an unwanted overhead in the maintenance of this repository as every time a change is made in one of the other two repositories (STIX/MISP Object templates hosted in different repositories) it would also require to reflect the changes here.

A reference conversion process is as follows:

* From STIX 2.1 Course of Action object with Security Playbook extension to MISP Security Playbook object:
<p align="left">
  <img src="/stix-to-misp-translation.png"/>
</p>

* From MISP Security Playbook object to STIX 2.1 Course of Action object with Security Playbook extension:
<p align="left">
  <img src="/misp-to-stix-translation.png"/>
</p>

### Mapping between STIX 2.1 Security Playbook extension and MISP Security Playbook object template
|STIX Property Name| MISP Attribute Name |
| :--- | :--- |
|**playbook_id**| **playbook-id**| 
|**description**| **description**|
| **created**| **-**|
| **modified**|**-**|
| **revoked**| **revoked**|
| **playbook_creation_time**| **playbook-creation-time**|
| **playbook_modification_time**| **playbook-modification-time**|
| **playbook_valid_from**| **playbook-valid-from**|
| **playbook_valid_until**| **playbook-valid-until**|
| **playbook_creator** | **playbook-creator**|
| **labels**| **labels**|
| **organization_type**| **organization-type**|
| **playbook_standard**| **playbook-standard**|
| **playbook_abstraction**| **playbook-abstraction**|
| **playbook_type**| **playbook-type**|
| **playbook_impact**| **playbook-impact**|
| **playbook_severity**| **playbook-severity**|
| **playbook_priority**| **playbook-priority**|
|**-**| **playbook-file**|
| **playbook_bin**| **playbook-base64**|

## Acknowledgments
This research was partially supported by the research project JCOP (Grant No. INEA/CEF/ICT/A2020/2373266), funded by the European Health and Digital Executive Agency through the Connected Europe Facility (CEF) program. 
