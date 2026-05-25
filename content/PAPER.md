# Open-Source Authoring and Publishing

## Abstract

Fill later

## 1 Introduction

The media and methods of information is tightly related with the pace of human progress. The arrival of computer technology, internet and large language models have deeply revolutionized the way that humans create and share knowledge. While nowadays academic publications, or intellectual commons in general, that are meant to be disseminated for public good, are largely trapped inside an outdated, printing-centered, and exclusive enclosure that hinders participation and sharing.

In traditional model, the authoring process is opaque; the publishing is oligopolistic; and after publishing, the access is plutocratic. As a catalyst, the training of large language models needs huge amount of machine-readable data in the public domain. The privileged access and outdated binary data (PDF) have created large barriers for those models to perform well in research tasks (**CITE**).

Open-source software thrived since the end of the 20th century due to its freedom of access, participation and deviation, which is also the major driving force of the advancement in information technology and the resulting economic booming (**CITE**). The methodologies involved in open-source development lifecycle, including source repositories, version control, continuous integration, issues and pull requests, are valuable practices to be integrated into the future of academic writing.

The ossified authoring and publishing model must be completely discarded in favor of a more egalitarian academia, where everyone can freely access, contribute, attest, and attribute the intellectual commons. This document will access the limitations in traditional model, elaborate on the new system, and envision the socio-economic impact of open-source authoring and publishing.

## 2 Limitations in Traditional Model

### 2.1 Exclusive Participation

In traditional journals, manuscripts are sent to submission systems, those systems often require ORCID and institutional email addresses (**CITE**), which creates a barrier for people with no institutional backgrounds. Even if the submission succeeds, desk rejection will almost certainly happen on the works with unauthoritative or unverifiable author identities. Moreover, assuming even desk rejection does not happen, in the peer review phase, single-blind reviewers often have bias toward manuscript authors with low profile. With all aforesaid factors combined, academical publishing has been essentially restricted to researchers inside universities and labs only.

### 2.2 Plutocratic Access

Once a manuscript is accepted by a journal, old-school journals often require transfer of copyright or exclusive publish right (**CITE**). These protocols directly infringes with the fact that academic results are meant to be the shared knowledge of human progress, instead of properties of proprietary companies. To allow the free access for all, researchers are often required to pay for a large amount of Article Processing Charges (APC) themselves. This created another layer of bias that only researchers with wealthy backgrounds or abundant funding can allow their own works to be accessible by other researchers.

If APC are not payed, the academic works will be locked behind a paywall of subscription fees, which reinforces the barriers toward the access of them for common citizens or underfunded researchers.

Researchers and libraries who subscribe journals are often nationally funded by the government. The research and peer review works are largely free labor where researchers spend time and equipment into researches without receiving profit. While journals are till charging high APC and subscription fees on readers. A unidirectional chain of value flow has formed, where journal publishers directly or indirectly exploit taxpayers, researchers, and government workers for private profits with low marginal cost (**CITE**), as well as creating negative societal externalities that hinders the access of academic resources from citizens and researchers to comprehend the latest advancements.

![[Exploitation.canvas]]

### 2.3 Opaque Authoring and Obsolete Medium

The only way that authorship is entitled to a academic paper is via the Authors list under the headline. This list fails to identify the individual contributions of the authors and does not provide a method of provenance. And in practice, authorship coercion happens from time to time among research papers (**CITE**). The lack of responsibility verification makes large scale academic misconduct and free problem possible, which harms academic fairness.

The majority of academic works are still published in the format of PDF, which is designed for human reading and printing. Researchers cannot embed interactive media and charts, executable research code, nor the dataset involved in researches. This absence of supporting material in research papers makes them irreproducible and experiment result fabrication becomes possible. This format also lacks the interactivity and interoperability presented in modern web-based presentation formats, making the work less comprehensible to people outside of the research world.

With the recent development of large language models, machine-readable training data in the public domain are demanded more than ever. However, due to the private ownership of journal publishers over research papers, and the nature of PDF that is less digestible by machines than plain text formats, an obstacle is formed between LLM participation and professional research fields. Researches have proven that large amount of open data will hugely improve the capability of LLMs in the corresponding field (**CITE**), the inaccessibility of closed format may cause long-term insufficiency in LLM participation in research works, potentially slowing down the pace of academic progress.

## 3 Prior Art Review

### 3.1 Academic Writing as Software Development

### 3.2 Revolutions in Publishing Routine

### 3.3 Political Economic Arguments

### 3.4 Pilots and Early Advocates

## 4 The New Architecture

### 4.1 Git Repositories and Authoring

The medium of the new manuscript drafting will be Git Repositories hosted on Git hosting services like GitHub and GitLab. Authors draft papers by making _commits_ or _pull requests_. Instead of opaque document drafting, open-source authoring or development in general often follow the collaboration workflow as follows:

1. The initiator, often one of the authors, creates a local Git repository.
2. He or she also creates a remote repository in Git hosting services as a shared source of truth, and link it to the local repository. Then an initial commit is made to populate the remote repository with basic setup.
3. Depending on the rigorousness of the authoring process, rigorous initiators often protect the `main` branch of the repository; other authors obtain a copy of the repository by creating a _fork_. In simple setups, the initiator grants other authors _write_ access while they obtain a copy by _cloning_ the repository.
4. Then authors conduct researches, record data in files, and draft their part of the paper. They frequently _commit_ or create _pull requests_ to the main branch to save their work.
5. Authors also frequently _fast forward_ their local repository to make their local copy aligned with the remote.
6. When the work is finished, a _tag_ is issued in the remote repository and a release is triggered. An automated pipeline will bundle the main paper into HTML and PDF formats with other repository files. Then it will automatically mint a DOI, upload the PDF to public archives, and deploy the website with the full content and metadata. This will be covered in detail in [[#4.3 Versioning and Publishing]].

By hosting the paper authoring in a public Git repository, the activity of the authoring process becomes fully transparent. Anyone with an eligible account of the Git hosting service can view the editing history directly via the service's web interface. This provides the most accurate insights into the contribution of each author, which eliminates ambiguities between individuals in terms of attribution and copyright. By analysing the Git history using professional tools, potential plagiarism and authorship coercion could be detected and flagged.

The Git paper authoring lifecycle also facilitates free collaboration, participation, and access of the writing process and content of the work. In modern open-source software development lifecycle, common users can report bugs via _issues_, they can contribute to the development process themselves by forking the repository and create their own _pull requests_. Some Git hosting services, like GitHub, also provide _discussions_ to ask questions or discuss about implementations. The open-source authoring process can be opt-in these integrated features. People with constructive ideas but zero institutional ideas can also create their own pull requests in writing the paper and add themselves to the authors list. Moreover, with this liberated infrastructure, everyone will be able to publish or access an academic work publicly, regardless of economic or institutional background.

With development pipelines like _continuous integration_ and _version control_ capability via Git, the quality control and publishing process will be highly automated; and the publications will be more error-tolerant and up to date. Basic continuous integration can automatically check for formatting, spelling and citation issues when a pull request is launched. While versioning function allows an open-source publication to release version 1.0.1 after being identified with several methodological flaws in 1.0.0. The new version will have a new DOI, PDF and the hosted website will also be redeployed once 1.0.1 release is triggered. Version control also makes catalog-style long term observations possible, where researchers take years long observations on a research subject, periodically record data and commit to remote Git repository, as well as drafting and publishing versioned catalogs on the findings over the last period.

The content of the open-source authored work will center around machine-readable formats, such as Markdown or Jupyter Notebook for text content, CSV for datasets and raw source code for programs. Researchers can commit any file to the repository, meanwhile, researchers should ensure that:

- All experiment conclusions and calculated results, together with how they are produced (manual review or code), should be either cited from authentic sources, or committed to the repository as files to ensure reproducibility.

This requirement, together with machine-readable formats, not only makes the researches described in the paper reproducible, but also makes AI agents navigate better inside a research repository (**CITE**), accelerating the research process. The entire repository, which contains the full paper content and all the data, will become public AI training data that help the advancement of LLM intelligence.

Some other open-source development approaches such as _monorepo_ can also be integrated into the repository to improve the efficiency and standardize drafting process.

### 4.2 The Unified Toolchain

During development, software developers often use various tools (DevOps) to automate routines. Open-source authoring and publishing also deserves a tool. While several tools exist (**CITE**), none have successfully streamlined the processes for the entire workflow or non-technical researchers. A successful tool should be usable in both continuous integration pipelines and researchers' daily operations, and should be extensible to suit various workflows.

We propose an unified toolchain for open-source researches - the `osap` which stands for open-source authoring and publishing. This tool will be build in a modular style with both command line interface and graphic user interface, each module will wrap around existing tools for swift development and compatibility.

While extensible via modules, `osap` should primarily serve for the following purposes:

- provides a simplified Git interface for non-technical researchers
- provides basic file formatting and spell check for continuous integration
- provides citation management and automatic retrieval
- provides a static site generator and PDF renderer for parsing the raw paper to established formats
- provides a publishing pipeline that integrates into the legacy system

Inspired by declarative package managers, the behavior of `osap` can be configured by `meta.yaml` inside the repository, an example `meta.yaml` could be like:

```yaml
title: Open-Source Authoring and Publishing
description: A synthesis of a democratized authoring and publishing framework for the creative publications in the post-AI era.
version: 0.0.1
keywords:
  - open-source
  - publishing
lang: en
authors:
  - given: Jean
    family: Valjean
    ocid: 8765-4321-1234-5678
    account: https://github.com/im-jean-valjean
    email: jean@valjean.ac.uk
repository: https://github.com/im-jean-valjean/osap
website: https://osap.valjean.ac.uk
pid: "doi:12345/9AAB.BCCD"
license: CC BY 4.0
type: article
entry: ./content/PAPER.md
citation-style: apa
```

This file configures default `osap` behavior and determines the metadata of the published paper, which is essential when integrating into the existing system.

`osap` core will be only a module loader and inter-process communication layer, while modules serve for distinct purposes. Modules are developed in bare programmatic APIs, and the CLI and GUI are simply another layer of wrapper above modules.

The Git module will be a wrapper around Git and Git hosting service APIs, it will provide the following functionalities:
- a user-friendly simplification of common commands in daily workflow, such as `branch`, `push`, `pull`, `commit`
- automatic execution of `fetch` and fast forward
- intuitive pull request, issue, discussion, version provenance and CI pipeline editing capability

The formatting module will wrap around existing tools like `oxfmt` and `cspell` (**CITE**) and integrate into CI pipelines.

The citation management module could reuse `manubot.cite` that

### 4.3 Versioning and Publishing

## 5 Socio-Economic Vision

## 6 Limitations and Mitigation

## 7 Conclusion
