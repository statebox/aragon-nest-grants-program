# Aragon Nest Proposal: Visual process modelling with Statebox

## Abstract

Statebox is a Turing incomplete language for protocols, whose preferred syntax is diagrams.

The language is build around a mathematical theory that is sufficiently abstract that it allows translation of diagrams into different many different domains: frontend (JS), backend, offchain (WASM), smart contract (EVM/WASM), etc.

Besides the natural fit of diagrammatic languages to workflow modelling, the category theoretic underpinnings allow us to construct correctness proofs of the translation of diagrams to code or proof the non-existence of deadlock in a user supplied workflow.

Many organisations have specialised workflows such as employee onboarding, budget approvals, etc. For example, if two people must approve something, one could model this as follows:

![](https://i.imgur.com/zIpsohN.gif)

We propose to investigate and implement a (proof of concept) backend for Statebox that would allow people to create customised workflows that "glue together" various Aragon services and enforce a certain process-like contract, without having to write any Solidity.


## Deliverables

1. A tool that compiles Statebox protocols into AragonOS or AragonJS compatible code
2. A example library of 'base protocols' that match some AragonOS provided services
4. A web interface to view the protocols and execution history and fire state transitions

## Grant size

Funding: Up to $100k in ETH, split into chunks paid out over achieved deliverables.
Success reward: Up to $50k in ANT, given out when all deliverables are ready.

## Application requirements

- **Theory**: The mathematics used by Statebox is outlined in a document that we call ["The Monograph"](https://archive.statebox.org/#/documents/monograph)

- **Typedefs** To describe, in a PL independent way, the types on "wires" we developed an alternative to protocol buffers, this project can be seen on github.com/typedefs

- **Studio** Our "process modelling IDE" is under development and not yet suitable for outside developers, but in any case, it can be browsed here https://statebox-studio-test.netlify.com

- **Team** We are probably be only company in the world that employs 7 Idris programmers! see [`team.md`](https://github.com/statebox/aragon-nest-grants-program/blob/master/grants/Statebox/team.md)

- **Burn**: About 25k/month for 10+ people; hard to say upfront what percentage of this would be allotted to this Aragon project.

- **Legal Structure**: Currently the software is developed by the for-profit company  https://statebox.io (wih me being the sole investor). We also setup a Dutch not-for-profit foundation https://statebox.nl that is supposed to take over ownership etc, to ensure the project persists in the long term.


## Development timeline

A rough development timeline would be the following:

| Deliverable           | Duration |
|-----------------------|----------|
| Initial Investigation | 2 weeks  |
| Example base protocol | 2 weeks  |
| Prototype compiler    | 2 months | 
| Prototype front end   | 2 months | 
| Round up              | 1 month  | 

Please note that

1) The main difficulty lies in understanding Aragon at depth and working out the details translation, hence we start with a proof of concept and then hope to follow up with a more concrete and detailed proposal based on our learnings.
2) The Statebox language implementation is currently still very restricted, which means that many real world processes cannot be implemented, yet.

Thus keep in mind that this proposal is about "demonstrating a vision of the future ", rather than developing a production ready tool.

