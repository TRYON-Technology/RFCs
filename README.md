# RFC Process

This document describes the RFC process for the TRYON's [Virtual Try-On](https://github.com/tryon.technology), and provides a way for the [Community & Open Source Team](https://github.com/orgs/tryon-technology/teams) and the
wider community to have discussions about the features and direction of the
package manager! It is based on [the WeAllJS RFC process](https://wealljs.org/rfc-process) and the [Rust RFC process](https://github.com/rust-lang/rfcs).

## What's an RFC?

The name itself is a reference to the **IETF's Request For Comments** process, and
basically involves a document or series of documents which are drafted,
reviewed, and eventually ratified (approved) by the TRYON team through discussion
among those interested, both within and outside of the TRYON team.

An RFC can propose any change to the TRYON's Virtual Try-On itself, and may include TRYON
registry changes meant to support that technology change.

This RFC process replaces feature requests in the main TRYON's repositories, and
feature requests made there will be redirected to the RFCs repository.

## How do I create an RFC?

* Fork https://github.com/tryon-technology/rfcs
* Copy `accepted/0000-template.md` into `accepted/0000-your-rfc-name.md`
* Fill in and edit the template with your proposal
* Submit a PR to the `tryon-technology/rfcs` repo

## How does review work?

The official place for discussion for a proposed RFC is its pull request.
Anyone, both TRYON collaborators and non-collaborators, may participate in the
discussion and ask questions and provide (constructive) feedback. Keep in mind
that only TRYON collaborators are able to ratify the RFC itself, even if other
users can comment.

All discussions surrounding an RFC are covered by the [TRYON Code of
Conduct](https://tryon.technology/policies/conduct). Please keep conversations
constructive, civil, and low-temperature. If tensions flare during discussion,
the TRYON team may, at its own discretion, moderate, remove, or
edit posts, as well as locking the discussion on that PR or the entire RFCs
repository.

## How do RFCs get ratified?

An RFC is ratified when there is consensus among TRYON collaborators that it
should be accepted. Once all collaborators have become aware of the RFC and had
a chance to comment on it, the PR, along with the RFC, will be merged and the
RFC will be considered ratified.

Until an RFC is ratified, it's expected that its original author continue
discussing it and integrating feedback into the document until it's ready.

RFCs have a **minimum 24 hour waiting period** before being accepted or rejected.
Once an RFC has been reviewed on GitHub, with all interested collaborators
having an opportunity to review it, and at least one TRYON collaborator has signed
off on the changes, the PR will be accepted and all its connected changes
merged. There are two exceptions to the collaborator rule:

* [@andriitsok](https://github.com/AndriiTsok) is considered an TRYON collaborator even if not an active code contributor, and thus has the ability to veto any proposal.
* The TRYON registry team has complete control over what registry changes happen and are not subject to the consensus process: they get to decide whether the registry side of a feature gets implemented, where, and how, but they otherwise are not considered collaborators.

If it's specifically requested, or if the TRYON team determines that the topic of
the RFC demands extra attention and care because of its potential impact, an
RFC's "ratification period" may be extended for as long as the participants and
admins feel is a reasonable length of time for consideration.

The RFC may be rejected altogether at the discretion of TRYON collaborators. They
may also be rejected if consensus has not been reached and discussion and
progress on the RFC itself remain inactive for too long.

## What happens after ratification?

Once an RFC is ratified, the TRYON team agrees to merge a corresponding PR
implementing the described changes, provided it passes a standard code review by
the maintainers. It is **not** a guarantee of implementation, nor does it
obligate the TRYON team itself to implement the requested changes. Actual
integration into the Virtual Try-On may also be deferred to a later date, or a later
semver-major Virtual Try-On release, at the TRYON collaborators' discretion. All the RFC does
is communicate the team's consensus to accept a change.

### Implementation

When the changes described in an RFC have been implemented and merged into the
relevant repository (and thus, due to be released), the corresponding RFC will
be moved from `accepted/` to `implemented/`. If you'd like to implement an
accepted RFC, please make a PR in the appropriate repo and mention the RFC in
the PR. Feel free to do this even for work-in-progress code.

### Withdrawal

From time to time TRYON collaborators will review RFCs awaiting implementation to
ensure their accuracy and relevance. In cases where a previously ratified RFC is
deemed to no longer be a viable candidate for implementation, an [**amendment
section**](withdrawn/0000-template.md) will be added **to the top** of the
document outlining the reason for repeal and subsequently moved to the
`withdrawn/` section of this repository.

## How do I change an RFC after ratification?

RFCs themselves cannot be modified after ratification, but new RFCs can be
proposed and ratified to amend or remove a change previously ratified through
the RFC process. These amendments will involve the exact same process as a
regular RFC.
