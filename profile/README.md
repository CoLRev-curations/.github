# CoLRev curations

Welcome to the CoLRev curations.

The purpose of **metadata curations** is to provide record metadata (authors, title, year, etc.) that is considered the single correct version.
Such curations rely on two principles: (1) Functionality that enables **efficient feedback cycles gathering corrections from the community**, and (2) **curators who review and accept corrections** (guarantors of quality).

Building on metadata curations, **content curations**, as separate CoLRev repositories, can provide additional and alternative layers of interpretation. For example, these could be annotations related to research methods, membership in research streams (topics), theoretical foundations, or findings.

## Using curations

To install a CoLRev curation (such as [MIS Quarterly](https://github.com/CoLRev-curations/mis-quarterly)), run

```
colrev env --install geritwagner/mis-quarterly
colrev env -i
```
With this setup, curated metadata will be used in the `load`, `prep`, `dedupe`, `pdf-prep`, `pull`, and `search` operations.

## Contributing to curations

The main path for community contributions to curated repositories is through pull requests.
The most convenient way to create a pull request is to change curated records in a CoLRev repository, commit them, and run `colrev push -r` (as suggested by `colrev status`).

## Creating curations

To create a new masterdata curation, run

```
colrev init --type colrev_built_in.curated_masterdata
# add crossref
colrev search -a "crossref:jissn=123456"
# add further sources (like DBLP)

```
