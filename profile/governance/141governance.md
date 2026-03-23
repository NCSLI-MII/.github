# Governance of NCSLI’s Measurement Information Infrastructure Products

## Contents

[Readers’ Guide](#readers-guide)

[Forward](#forward)

[Acknowledgments](#acknowledgments)

[Purpose and Scope](#purpose-and-scope)

[Executive Summary](#executive-summary)

[General Governance](#general-governance)

[MII Project Governance](#mii-project-governance)

[Coordinators](#coordinators)

[Reviewers](#reviewers)

[Committers](#committers)

[Contributors](#contributors)

[Users](#users)

[Process Flow](#process-flow)  
[http://sage.grad.hr:1234/doc/static/developer/workflows.html](#process-flow)

[Concepts](#concepts)

[References](#references)

[Copyright](#copyright)

## Readers Guide

This document outlines the best practices for governing the development, approval, and release of MII products.
Stakeholders include both scientific organizations and the international quality infrastructure, e.g., metrology institutes, standards organizations, accreditation organizations and bodies, legal metrology organizations, test and calibration laboratories, software providers, instrument manufacturers

**Forward**—summarizes the purpose and scope of the document and acknowledges the individuals and organizations who contributed.

**Governance**—describes the overall governance.

**MII Project Governance**—outlines specific goverance procedures and structures for MII projects, including roles and responsibilities.

**Concepts**—explains acronyms and special terms used herein.

**Copyright**—specifies the terms of use.

## Forward

This document describes and develops industry best practices for governing the development, approval, and release of MII products.

Please direct comments and questions concerning the contents of this publication to the NCSLI 141 MII and Automation Committee (henceforth called the "MII\&AC"), accessible through NCSL International, 800 Roosevelt Road, Building C, Suite 312, Glen Ellyn, IL 60137 or through its GitHub web site (https://github.com/NCSLI-MII).

### Acknowledgments

The NCSLI comprises member delegates and others within the metrology community with expertise in metrology and automation.
NCSLI members who contributed to this document represent a variety of organizations, large and small, engaged in managing metrology data.

#### First Edition

The MII\&AC members who contributed to the first edition include:

| Name | Organization |
| :---- | :---- |
| Mark Kuster | 141 MII\&AC Chair |
| Michael Schwartz | Cal Lab Solutions |
| Colin Walker | IndySoft |
| Ryan White | National Research Council of Canada |
| David Wolfe | Cal Lab Solutions |

The MII\&AC also acknowledges the many non-MII\&AC NCSLI members, the NCSLI Board of Directors, and other interested parties who provided valuable comments and suggestions.
See the GitHub issue and change management history for further information on contributors.

This document’s formatting generally follows the NCSLI style guide (NCSLI, 2013\) but may deviate as required.

### Purpose and Scope

This document establishes the requirements for the development, approval and release of open-source MII products.

This document applies to all open-source MII\&AC products, including but not limited to

1) specification documents,
2) the measurand taxonomy,
3) the M-layer,
4) other published schemas, data models, reference data, etc.,
5) the governance document(s) themselves.

### Executive Summary

NCSLI chartered the MII\&AC to address the large volume and cost of unstructured measurement-related data flows between producers and consumers worldwide.
Much of this data flow incurs excessive cost for lack of interoperability, machine-readability and machine-actionability.
The MII\&AC intends to develop and publish metrology-information models, metrology-process models and reference metadata sets to standardize digital metrology data.
Such data includes measurement results in calibration certificates, calibration and measurement capabilities in accreditation scopes, instrument specifications, and other related information.
The MII\&AC or its subcommittees will present its products to NCSLI members and the metrology community under an open-source license.
The published products together form a measurement-information infrastructure (MII).

Toward these ends, this document governs the development, maintenance and use of MII products so as to encourage participation and use in digital-transformation solutions while maintaining unambiguous conceptual models and reference data for free and open use.

## General Governance

Governance shall first and foremost follow NCSLI’s current *Committee Chair Handbook* (NCSLI, 2014).
Upon the handbook’s revision, the 141 Committee shall review the changes and either

1) adopt the changes as applicable,  
2) request a waiver from the NCSLI board of directors regarding problematic issues or  
3) pursue changes to the committee handbook to resolve the problem(s).

This document, along with the online *Development Guide*, provides MII-specific governing rules not addressed in the NCSLI *Committee Chair Handbook*.

## MII Project Governance 

This section takes inspiration from the Apache Software Foundation’s governance of Apache projects ([A Primer on ASF Governance | Apache Software Foundation](https://www.apache.org/foundation/governance/)) to implement NCSLI policies in MII\&AC operations using online project-management tools.
All processes herein shall conform to the NCSLI *Committee Chair Handbook*.
The MII\&AC’s online *Development Guide* provides low-level details and shall adhere to both this document and the NCSLI *Committee Chair Handbook*.

An RG (responsible group) owns and manages each MII product.
The MII\&AC determines whether to designate a WG (working group) or itself as the RG for each product.
The RG establishes one or more milestone specifications for each product release through consensus and approves those milestone specifications by a formal vote.
RG members and other participants develop the product to meet its established milestone specifications.
Before release, the RG validates the release’s conformance to its approved specifications by a formal vote.

Anyone may participate in specification development, but only established voting members may vote.
Participants may freely serve in the role of Contributor or User, or if appointed, as a Reviewer, Coordinator, or Committer.
The RGCs determine a product’s relevant voting members according to the NCSLI *Committee Chair Handbook*.
In general, NCSLI allows worldwide membership without restriction.
To maximize the online system’s value, the MII\&AC shall conduct the voting process in writing through the online system if-when feasible and in MII\&AC or WG meetings otherwise.
Each RG Chair (RGC) shall maintain its voting roster on the online system.

The RGC directly or indirectly designates qualified and willing participants and members for specific roles on projects within the RG’s scope.
The RGC may also revoke appointments per the NCSLI *Committee Chair Handbook*.
In small project teams, team members may assume multiple, but non-conflicting, roles.
Several defined roles within the MII\&AC support the development, maintenance, and governance of MII products:

### Coordinators 

The RGC appoints one or more coordinators for each product within the RG’s scope.
The RGC may also serve as a coordinator.
Coordinator candidates shall have voting rights per the NCSLI *Committee Chair Handbook*.

Coordinators manage release validation to ensure the product meets its approved milestone specification, track and resolve all issues in time for release validation, open new issues during the validation process, and tag releases.
Coordinators also publish releases after RG approval.

### Reviewers 

The RGC appoints reviewers from the RG membership who have shown sufficient interest and subject or technical knowledge to review contributions from the community.
Committers may also serve as reviewers.

One or more reviewers evaluate and comment on each proposed contribution, question, or suggestion toward releasing a product.
The reviewers’ work should provide the required information for committers and the RG to judge compliance to the product’s current milestone specifications to streamline the creation and approval of new releases.
Reviewers shall not review their own contributions.

### Committers 

Either coordinators or the RGC appoint committers from the RG membership who have shown merit within their project as contributors or in other roles.
Coordinators shall ensure that each product within the RG’s scope has one or more committers and grant each committer sufficient access to the project on the online system.

Committers approve contributions and commit them to the designated product release.
Committers help ensure product quality for safe release under the MII open-source license.

### Contributors 

Contributors volunteer from the community at large and require no appointment.
Contributors equate to RG participants or members depending on their NCSLI membership status.

Contributors contribute source-code, data, metadata or documentation, and may help with release validation, meetings, mailing lists, and workshops.
Contributors do not have a specific governance role; however, healthy projects always seek productive and helpful contributors whom they may consider nominating as new committers.

### Users 

Users may have NCSLI memberships or not, have no governance role, and may freely access MII products.
They use and often request help with MII products.
Many helpful users do not develop products per se but still spend time submitting bug reports and answering questions.
Users may also include developers who incorporate MII products into their own products.
Such users should consider contributing to MII-product release validations.

As a natural consequence of experience and interest, contributors may eventually become committers.
Likewise, committers may become reviewers, who may become coordinators.

### Process Flow 

1. Anyone may open a GitHub issue outlining a proposed contribution or suggested improvement.  
   1. Contributors submit milestones as an issue or set of issues for ease of management and workflow.
2. A reviewer comments on the issue–its validity, relevance, type (labeling it as a bug fix, documentation change, new development, …)–and identifies what, if any, milestone it applies to.  
3. The reviewer may:  
   1. Close the issue as invalid or irrelevant after commenting on the issue  
   2. Ask for further detail and or supporting documentation  
   3. Request another reviewer’s input  
   4. Request RG or RGC input
   5. Move the issue to RG voting members
4. The contributor(s) works on the issue(s) and submits a push request with the changes for review.
5. The reviewer checks the changes then:  
   1. Approve the changes by checking against the issue or milestone requirements  
   2. Rejects the changes, adding comments for the contributor to modify the changes and resubmit  
6. A committer, once all or a significant number of push requests pass reviews, then commits the changes to a release version or pre-release version.
7. Users (and beta testers) may pull the latest or previously released version of the files and data.

## Concepts

### Acronyms 

| Acryonym | Meaning |
| :---- | :---- |
| CC | NCSLI committee chair |
| MII | Measurement Information Infrastructure |
| MII\&AC | MII and Automation Committee |
| RG | responsible group; either the MII\&AC itself or the specific WG responsible for a given product |
| RGC | RG chair; the WGC or CC |
| WG | MII\&AC working group |
| WGC | MII\&AC WG chair |

### Definitions 

| Term | Meaning |
| :---- | :---- |
| GitHub | a website resource used for source code & document management |
| MII product | any document, software or data set that the MII\&AC develops, approves and releases
| online system | NCSLI GitHub web site, backed up by the NCSLI web site as required |
| participant | NCSLI members and non-members who attend, contribute, or participate in MII\&AC activities |

### Verbal Forms 

For clarity, this document uses specific verbal forms to express requirements, recommendations, permissions, and their negations.
Readers will find the usage similar to the ISO-IEC specification \\cite{ISO:DirectivesP2}.

#### Requirements 

Compliance to this document means adherence to all relevant requirements (including negative requirements–prohibitions).
The verbal forms “shall” and “shall not” identify all requirements and prohibitions, respectively, and never express any other meaning.

#### Recommendations 

The verbal forms “should” and “should not” express recommendations, such as the preferred (or deprecated) choice of multiple options.

#### Permission 

The verbal form “may” expresses permission.
The form “may not” does not express a prohibition but rather permission for the negative.
For example, “may not include” means "may (not include)" or "may omit".
To avoid confusion, this document uses the latter form.

#### Other Verbal Forms 

This document avoids redundant, ambiguous or inappropriately absolute terms such as "can", "need", "must", their equivalents and their negations.

## References 

- GitHub. *GitHub*. GitHub: Let's build from here · GitHub. Retrieved August 26, 2024, from https://github.com/
- NCSLI. (2013). *Technical Publications Style Guide*. NCSL International. Retrieved Aug 19, 2024, from https://ncsli.org/members/group\_content\_view.asp?group=232595\&id=907954  
- NCSLI. (2014). *Committee Chair Handbook* (20140506). NCSL International. Retrieved Aug 19, 2024, from https://ncsli.org/members/group\_content\_view.asp?group=232595\&id=907953

## Copyright 

Copyright © 2024 (and when generated) by NCSL International.
All rights reserved

### MII-Product Use

Organizations creating products and projects for use with MII products should take care to respect the CC-BY-SA license.
The MII\&AC encourages organizations to document their use cases by sharing the organization, URL, MII products used in the project, and a short description of the use case.

### Permission To Reproduce 

NCSL International (NCSLI) grants permission to use the material contained in this publication, including reproduction of part or all of its pages, according to the Creative Commons Attribution-ShareAlike 4.0 International Public License, found at https://creativecommons.org/licenses/by-sa/4.0/legalcode.en, and the following conditions:

1\) The words “NCSL International Technical Publication” appears on each page reproduced.  
2\) The disclaimer hereafter is incorporated into any reproduction of the publication.

### Permission To Translate 

Permission to translate part or all of this publication is granted, provided that the following conditions are met:

1\) The words “Translated by \[translator's name\]” appear on each page translated.  
2\) The following disclaimer is incorporated into any reproduction of the publication.
If a translation is copyrighted, the translation must carry a copyright notice for both the translation and the publication from which it is translated.

### Disclaimer

The materials and information contained herein are provided and promulgated as an industry aid and guide, and are based on standards, formulae, and techniques recognized by NCSL International.
The materials are prepared without reference to any specific federal, state, or local laws or regulations, and NCSL International does not warrant or guarantee any specific result when relied upon.
The materials provide a guide or recommended practices and are not all-inclusive.

From time-to-time commercial equipment, instruments, or materials are identified in technical publications to foster understanding.
Such identification does not imply recommendation or endorsement by the NCSL International, nor does it imply that the materials or equipment identified are necessarily the best available for the purpose.
