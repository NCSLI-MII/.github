# GitHub Development Guide for NCSLI’s Measurement Information Infrastructure Products

This document remains rough and incomplete. It may also contain high-level information that we should move to the main Governance document instead.

## Contents

[Forward](#forward)

[GitHub Implementation](#github-implementation)

[GitHub Rules](#github-rules)

[Access Rules](#access-rules)

[Change Management](#change-management)

[Change Classification and Versioning](#change-classification-and-versioning)

[Major Changes](#major-changes)

[Minor changes](#minor-changes)

[Patching Changes](#patching-changes)

[Pre-release Updates](#pre-release-updates)

[Branching](#branching)

[Merges](#merges)

[Releases](#releases)

[Guidelines for Specific MII Products](#guidelines-for-specific-mii-products)

[Contents](#contents)

[Copyright](#copyright)

## Forward 

### Purpose and Scope 

This document provides specific guidelines for routine development, approval and release of MII products through the NCSLI 141 MII and Automation Committee (henceforth called the "MII\&AC").
This document’s contents do not require NCSLI Board of Directors approval.
This document’s development maintenance shall instead adhere to *Governance of NCSLI’s Measurement Information Infrastructure Products*, latest version, and the guidelines herein, as for any other MII product development.

Backlog for this document to address (driven by either the NCSLI Committee Handbook or MII Governance document):

1. Voting  
   1. Ensure that product releases happen only with at least two thirds of the RG’s participating voting members (quorum).
   Quorums require at least 51 % of the RG’s full voting membership.
   2. Define the place to maintain each product’s voting roster and RG membership.  
   3. Ensure that we state the motion under vote (a release) in positive terms, e.g. “Release M-Layer version x.xx”.  
   4. Record votes (with optional comments for RG review) in the GitHub process.  
   5. Document the comment resolution.  
   6. Allow at least 30 d for voting members to review the release candidate. (Hopefully this time overlaps at least some of the development time–maybe have voting members subscribe to all commits or something …)  
   7. Allow (only) voting members to abstain (no vote by the due date), disapprove, approve with comments, or approve without comments.  
2. Address the roles and access rights as applicable: coordinators, reviewers, committers, contributors, users, and any required details as to how they perform their responsibilities in GitHub.  
3. A place for each release’s draft and approved specifications

## GitHub Implementation 
The MII\&AC and WGs shall use the NCSLI MII GitHub site for official development and to implement the governance specified herein.
This MII Development Guide on GitHub specifies the development process detail that coordinators, committers, reviewers and contributors shall follow.

### GitHub Rules 

Edit this section to reflect the defined roles and responsibilities in the governance doc.

The MII\&AC's open-source work may be accessed and managed on GitHub.
To implement changes, one must be an NCSLI member, with appointed MII\&AC members having voting rights.
All changes, major or minor, will follow these rules.

#### Access Rules 

Everyone shall have read-only access to and use of MII products according to the product’s open-source license posted on GitHub and the [NCSLI copyright notice](https://docs.google.com/document/d/1zxWOWAsX6xjJRMDLcBGw30B4ntv4oi8aoEEeTHC1myE/edit#heading=h.7mi9vset2abm) herein.

Any stakeholder using the MII open-source products may suggest changes to the master branch in GitHub.
All major changes require MII\&AC approval by appointed members with voting rights.
All voting will follow NCSLI member voting guidelines.

### Change Management 

How do we specifically use GitHub processes to implement our governance?

#### Change Classification and Versioning

The repository will follow semantic versioning principles to increment version numbers to reflect changes.
The incrementation rules follow:

##### Major Changes 

Version increments by: 1.0.0  
Major changes introduce content that breaks functionality for existing users.
Breaking would take place any time existing content becomes more restrictive.
This would include editing the content of existing taxons, deprecating taxons, deleting content from taxons.

##### Minor Changes

Version increments by: 0.1.0  
Minor changes represent new, non-breaking additions to the repository.
Adding new taxons would be classified as minor.

##### Patching Changes

Version increments by: 0.0.1  
Patching changes add new content to existing taxons that do not affect existing users.
As an example, a patch change would add new references or optional parameters to existing taxons.

##### Pre-release Updates 

MII\&AC members will work to merge all working branches into a pre-release branch for the next released version of the product.
The pre-release cycle, before the first production 1.0.0 version is released, is following a Minor change versioning with the beta tag, e.g. 0.2.0-beta, 0.3.0-beta, etc...

#### Branching 

GitHub allows users to branch items, make changes, and merge those changes back into a working branch.

##### NCSLI Branches & Branch Management

**main** branch – the currently fully approved branch under major version control releases

**development** branch – branches the MII\&AC or working group currently edits. Working branches are recommended to be created from a reported issue. This ensures provenance can be traced to a resolved issue and subsequent pull request.
These branches may contain major, minor and patching changes. 

**pre-release** branch – branch currently staged for a MII\&AC approval vote for merging into the next main branch.

Note that pre-release and development branches are synonymous during the pre-release beta cycle.  

The MII\&AC will approve users with roles to manage the NCSLI branches.
The MII\&AC will assign the role of Coordinator, Committer, and Reviewer to members of the working group.
The Coordinator will group change requests into specific version releases.
The Reviewer will review and approve changes.
Once approved, the Committer will merge changes into the current Pre-Release Branch and main branch.

##### Stakeholder Branch Management

Any stakeholder may create a branch and manage a new version, with the eventual goal of merging those changes back into the official main branch through MII\&AC review and approval. Before creating a development branch, open an issue that describes the proposed changes. From the reported issue, create a branch for the issue then checkout the branch for development purposes. Once the changes are implemented, open a pull request.

#### Merges

Members creating development branches may assign roles to users, defining who may approve branch changes and commits back into that branch. The merge process(es) across MII repositories intends to be automated through customized github actions. The only mechanism to merge changes is through a Pull Request to **main** that triggers a multistep process. Committers may open Pull Requests, approve PRs and merge changes into **main**. In order to keep a linear commit history, **development** branch commits are squashed before merge, such that each change can be traced to a PR and issue.
- Schema changes validated against XML, JSON or other schema definitions.
- Any source changes are validated against the **development** branch schema.
- Successful validation requires at least one approving review.
- Upon approval, any further changes are automated and committed to the branch.
- The committer is now able to squash and merge changes into **main**.

#### Releases 

The Coordinator will create a working branch in Github and accept changes approved by Reviewers into the working branch.
The RG will prioritize and process changes based on the requirements of Contributors, Users, and the working group’s strategic priorities.
The Reviewer will provide a final sign-off on the scope of changes in a new branch.

After submission of a working branch, the MII\&AC will evaluate the working branch contents and summary and determine the level of changes that exist within the working branch and assign a change classification (Major, Minor, Patch).

The RG may merge working branches that meet the criteria of minor changes or patching changes into the main branch on approval from the MII\&AC.
The RG shall merge the approved working branch into the pre-release branch in parallel.

The RG shall merge working branches that meet the criteria of Major Change  into the Pre-Release Branch after a vote and approval of the MII\&AC.

The RG may then vote on the Pre-Release Branch and, if approved, merge it back into the main branch for a major version release.

NCSLI Major Releases  
It will require a MII\&AC vote to roll all changes in the pre-release branch into the main branch.

NCSLI Minor Changes or Patching Changes
Participants may approve minor changes and patches during weekly MII\&AC meetings.
The RG may merge those changes with negligible effects which do not require a major release approval into the main or pre-release branches.

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

## Guidelines for Specific MII Products 

### M-Layer
Those who wish to augment or otherwise refine the M-layer repository should also see the [Blair's doc].

### Measurand Taxonomy
Those who wish to augment or otherwise refine the taxonomy repository should also see the [measurand taxonomy guide].

## Concepts

### Acronyms 

| Acryonym | Meaning |
| :---- | :---- |
| CC | MII\&AC chair |
| CMC | calibration and measurement capability |
| MII | Measurement Information Infrastructure |
| MII\&AC | MII and Automation Committee |
| WCG | MII\&AC working group chair |

### Definitions 

| Term | Meaning |
| :---- | :---- |
| GitHub | a website resource used for source code & document management |

Refer to the MII Governance document for terms not defined herein.

## Copyright 

Copyright © 2024 (or year produced) by NCSL International. All rights reserved

### Permission To Reproduce 
NCSL International (NCSLI) grants permission to use the material contained in this publication, including reproduction of part or all of its pages, according to the Creative Commons Attribution-ShareAlike 4.0 International Public License, found https://creativecommons.org/licenses/by-sa/4.0/legalcode.en, and the following conditions:

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
