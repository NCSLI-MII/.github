# GitHub Development Guide for NCSLI’s Measurement Information Infrastructure Products

# Forward 

## Purpose and Scope 

This document provides specific guidelines for routine development, approval and release of MII products. This document’s contents do not require NCSLI Board of Directors approval. This document’s development maintenance shall instead adhere to *Governance of NCSLI’s Measurement Information Infrastructure Products*, latest version, and the guidelines herein, as for any other MII product development.

Contents

[Forward](#forward)

[Purpose and Scope](#purpose-and-scope)

[GitHub Implementation](#github-implementation)

[GitHub Rules](#github-rules)

[Access Rules](#access-rules)

[Change Management](#change-management)

[Change Classification, Versioning](#change-classification,-versioning)

[Major Changes](#major-changes)

[Minor Changes](#minor-changes)

[Patching Changes](#patching-changes)

[Pre-release Updates](#pre-release-updates)

[Branching](#branching)

[Merges](#merges-members-creating-working-branches-can-assign-roles-to-users,-defining-who-can-approve-branch-changes-and-mergers-back-into-that-branch.)  
[Members creating Working Branches can assign roles to users, defining who can approve branch changes and mergers back into that branch.](#merges-members-creating-working-branches-can-assign-roles-to-users,-defining-who-can-approve-branch-changes-and-mergers-back-into-that-branch.)

[Releases](#releases)

[Guidelines for Specific MII Products](#guidelines-for-specific-mii-products)

[M-Layer](#m-layer)

[Measurand Taxonomy](#measurand-taxonomy)

[CMCs](#cmcs)

[Glossary](#glossary)

[Acronyms](#acronyms)

[Terms and Definitions](#terms-and-definitions)

[Copyright](#copyright)

[Permission To Reproduce](#permission-to-reproduce)

[Permission To Translate](#permission-to-translate)

[Disclaimer](#disclaimer)

Backlog for this document to address (driven by either the NCSLI Committee Handbook or MII Governance document):

1. Voting  
   1. Ensure that product releases happen only with at least ⅔ of the RG’s voting members participating (quorum). Quorums require at least 51 % of the RG’s full voting membership.  
   2. Define the place to maintain each product’s voting roster and RG membership.  
   3. Ensure that we state the motion under vote (a release) in positive terms, e.g. “Release M-Layer version x.xx”.  
   4. Record votes (with optional comments for RG review) in the GitHub process.  
   5. Document the comment resolution.  
   6. Allow at least 30 d for voting members to review the release candidate. (Hopefully this time overlaps at least some of the development time–maybe have voting members subscribe to all commits or something …)  
   7. Allow (only) voting members to abstain (no vote by the due date), disapprove, approve with comments, or approve without comments.  
2. Address the roles and access rights as applicable: coordinators, reviewers, committers, contributors, users, and any required details as to how they perform their responsibilities in GitHub.  
3. A place for each release’s draft and approved specifications

# GitHub Implementation 
The NCSLI MII Committee and WGs shall use the NCSLI MII GitHub site for official development and to implement the governance specified herein. The *MII Development Guide* on GitHub specifies the development process detail that coordinators, committers, reviewers and contributors shall follow.

## GitHub Rules 

Edit this section to reflect the defined roles and responsibilities in the governance doc.

The MII committee's open-source work can be accessed and managed on GitHub. To propose changes, one must be an NCSLI member, with appointed committee members having voting rights.  All changes, major or minor, will follow these rules.

### Access Rules 

Everyone shall have read-only access to and use of MII products according to the product’s open-source license posted on GitHub and the [NCSLI copyright notice](https://docs.google.com/document/d/1zxWOWAsX6xjJRMDLcBGw30B4ntv4oi8aoEEeTHC1myE/edit#heading=h.7mi9vset2abm) herein.

Any stakeholder using the MII open-source products may suggest changes to the master branch in GitHub. All major changes require committee approval by appointed members with voting rights.

All voting will follow NCSLI member voting guidelines.

### Change Management 

How do we specifically use GitHub processes to implement our governance?

### Change Classification, Versioning 

As changes are introduced the repository will follow semantic versioning principles to increment version numbers standard. The incrementation rules are as follows:

#### Major Changes 

Version increments by: 1.0.0  
Major changes introduce content that breaks functionality for existing users. Breaking would take place any time existing content is altered to become more restrictive. This would include editing the content of existing taxons, deprecating taxons, deleting content from taxons.

#### Minor Changes 

Version increments by: 0.1.0  
Minor changes represent new, non-breaking additions to the repository. Adding new taxons would be classified as Minor.

#### Patching Changes 

Version increments by: 0.0.1  
Patching changes add new content to existing taxons that do not affect existing users. An example of a patch change would be adding new references or optional parameters to existing taxons.

#### Pre-release Updates 

Committee members will work to merge all working branches into a PreRelease branch for the next released version of the committee product.

#### Branching 

GitHub allows users to branch items, make changes, and merge those changes back into a working branch.

NCSLI Branches & Branch Management 

Main Branch \- is the main current / fully approved Branch under Major Version control releases. 

Working Branches are the current working branches the committee or committee working group is currently editing. These branches may contain both major and minor and patching changes.

The PreRelease Branch is a branch that is getting staged for committee vote and will be merged/updated into the next Master Branch.

Stakeholder Branch Management

Any stakeholder can create a branch and manage their unique taxon definitions, with the eventual goal of merging those changes back into the official master branch through committee review and approval.  

#### Merges Members creating Working Branches can assign roles to users, defining who can approve branch changes and mergers back into that branch.  

NCSLI Branches & Branch Management   
The 141 Committee will approve users with roles to manage the NCSLI branches. The committee will assign the role of Coordinator, Committer, and Reviewer to members of the working group. The Coordinator will group change requests into specific version releases. The Reviewer will review and approve changes. Once approved, the Committer will merge changes into the current Pre-Release Branch and Master Branch. 

#### Releases 

The Coordinator will create a Working Branch in Github and accept changes approved by Reviewers into the Working Branch. Changes are prioritized and processed based on the needs of Contributors, Users, and the working group’s strategic priorities.  When the branch is formed, the Reviewer will provide a final sign-off on the scope of changes. 

When a Working Branch is submitted to the 141 committee, the committee will evaluate the Working Branch contents and summary and determine the level of changes that exist within the Working Branch and assign a Change Classification (Major, Minor, Patch).

Working Branches that meet the criteria of Minor Changes or Patching Changes may be merged into the Master Branch on approval from the committee. The approved Working Branch shall be merged into the PreRelease Branch in parallel.

Working Branches that meet the criteria of Major Change shall be merged into the Pre-Release Branch after a vote and approval of the committee. 

The Pre-Release Branch can then be voted on and, if approved, merged back to the master branch for a major version release.

NCSL Major Releases  
It will require a committee vote rolling all changes in the pre-release branch into the Master Branch.

NCSL Minor Changes or  Patching Changes  
Minor changes and patches can be approved during weekly committee meetings. As long as their effects are negligible and do not require a major release approval, the changes can be merged into the master or pre-release branches.

**Specifications:**  
Taxonomy Definition Rules

Schema Version Management for (including but not limited to):  
	Taxonomy  
CMCs  
Instrument Functions  
Measurement Results

**CRUD Rules:**  
**Creating new taxa (generalize to all MII metadata types)**  
**Redistribution and Use**  
**Update and Modification of existing taxa**  
**Deprecation and Replacement of existing taxa**

# Guidelines for Specific MII Products 

## M-Layer 

## Measurand Taxonomy 

## CMCs

# Glossary 

## Acronyms 

| AB | accreditation body |
| :---- | :---- |
| BIPM | Bureau International des Poids et Mesures (International Bureau of Weights and Measures) |
| CC | NCSLI committee chair |
| CMC | calibration and measurement capability |
| ESI | embedded SI |
| GitHub | website resource used for source code & document management |
| KCDB | BIPM’s Key Comparison Database |
| JSON | JavaScript Object Notation |
| MII | Measurement Information Infrastructure |
| MQM | measurement quality metric |
| SI | BIPM’s système international (d’unités) \[international system (of units)\]  |
| SoA | statement of accreditation; accreditation statement |
| TBD | to be determined |
| WCG | NCSLI committee working group chair |
| XML | eXtensible markup language |
|  |  |
|  |  |

## Terms and Definitions 

Refer to the MII Governance document for terms not defined herein.

More definition stuff goes here…

# Copyright 

Copyright © 2024 (or year produced) by NCSL International. All rights reserved

## Permission To Reproduce 
NCSL International (NCSLI) grants permission to  use  the material contained in this publication, including reproduction of part or all of its pages, according to the Creative Commons Attribution-ShareAlike 4.0 International Public License, found https://creativecommons.org/licenses/by-sa/4.0/legalcode.en, and the following conditions:

1\) The words “NCSL International Technical Publication” appears on each page reproduced.  
2\) The disclaimer hereafter is incorporated into any reproduction of the publication.

## Permission To Translate 

Permission to translate part or all of this publication is granted, provided that the following conditions are met:

1\) The words “Translated by \[translator's name\]” appear on each page translated.  
2\) The following disclaimer is incorporated into any reproduction of the publication. If a translation is copyrighted, the translation must carry a copyright notice for both the translation and the publication from which it is translated.

## Disclaimer 

The materials and information contained herein are provided and promulgated as an industry aid and guide, and are based on standards, formulae, and techniques recognized by NCSL International. The materials are prepared without reference to any specific federal, state, or local laws or regulations, and NCSL International does not warrant or guarantee any specific result when relied upon. The materials provide a guide or recommended practices and are not all-inclusive.

From time-to-time commercial equipment, instruments, or materials are identified in technical publications to foster understanding. Such identification does not imply recommendation or endorsement by the NCSL International, nor does it imply that the materials or equipment identified are necessarily the best available for the purpose.
