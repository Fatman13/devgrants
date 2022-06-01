# RFP Proposal: `FVM - Go SDK`

**Name of Project:** FVM - Go/Tinygo SDK 

**Link to RFP:** 

**RFP Category:** `devtools-libraries`

**Proposer:** `hunjixin`

**Do you agree to open source all work you do on behalf of this RFP and dual-license under MIT, GPL, and APACHE2 licenses?:**  Yes

# Project Description

Since the announcement of [FVM](https://fvm.filecoin.io/), support for a broader developer community other than the native Rust programming language is of high importance to the FVM roadmap in general. A strong and diverse developer community has been proven to be critical to the longevity of a project and we think that FVM project have the opportunities to attract more developers with a wider SDK support.

During FVM Early Builder program, we have successfully built a PoC Go SDK that facilitates the use of Tinygo to write user-defined actors (smart contracts) that meets the requirement of WASM compilation target so that the said actors can be run in the WASM-based FVM execution environment. In extension of this PoC, we now propose the continuation of the development for the FVM GO SDK.

## Value

<!-- Please describe in more detail why this proposal is valuable for the Filecoin ecosystem. Answer the following questions: -->
<!-- - What are the benefits to getting this right? -->

The benefits of a Go SDK is apparent as it provides a much easier on-ramp for Go developers into the fvm ecosystem. In addition, the existing pool of contributors to Lotus and Venus implementation of Filecoin could jump right into fvm development with language they already familiar with. Some highlights FVM could leverage by bringing in Go SDK:

- A fairly easy-to-learn high-level programming language 
- An extensive selection of libraries, especially blockchain related ones
- Matches the technology stack of Filecoin which allows `import` of necessary libs

All in all, we believe that a Go SDK would contribute a great deal to the growth of the FVM ecosystem and could be the gateway language to on board more developers to write user-defined actors.

<!-- - What are the risks if you don't get it right? -->


<!-- - What are the risks that will make executing on this project difficult? -->

<!-- This section should be 1-3 paragraphs long. -->

## Development Roadmap and Deliverables

### Milestone 1 

Writing and executing actors using TinyGo.

**Deliverables**:

- go-fvm-sdk v0.1
- Implement all fvm system calls
- Implement test system tools
- Testing CI workflows   
- Basic documentation about FVM (technical, Usage, FAQ)
- Hello World and ERC20 examples

**Funding for this Milestone**:

**Estimated Milestone Delivery**:

Within time framework of early builder program. (End of July 22)

### Milestone 2 - EVM support

Taking advantage of the fact that EVM is written natively using Go, we plan to build a [Shim](https://en.wikipedia.org/wiki/Shim_(computing)) layer upon go-fvm-sdk as foundation and run Solidity code on top of it. 

**Deliverables**: 

- go-fvm-sdk v0.x
- Support evm code running in TinyGo
- Updated CI workflows
- Update Document for evm support

**Funding for this Milestone**:

**Estimated Milestone Delivery**: 

A month. (End of August 22)

### Milestone 3 - Memory optimization 

We expect that there could be performance issues given the native garbage collection. This could be amended by adopting manual memory allocation functions, which works similarly to dynamic memory allocation in C where user could allocate memory and free memory on demand. Thus, improves the performance of running actors. 

At the same time we expect to expose some basic types for managed code.

**Assumptions/Requirements**:

- Explore opportunities in Cgo and identify if minimal changes could allow Cgo to be compatible with WASM
- Manual memory management would require extra storage apart from ones designated to garbage collection, which may require support of memory allocation function of FVM

**Deliverables**:

Both data structures and utilities packages:
- go-fvm-sdk v0.x
- Extended documentation
- Updated CI workflows
- types like CString, CSlice（If necessary）
- Able to load WASM lib compiled from dynamic memory allocation of C or Rust
- Can properly handle the boundaries between managed and unmanaged code

**Funding for this Milestone**:

**Estimated Milestone Delivery**:

Three month. (End of Nov 22)

### Milestone 4 - Golang-fvm—sdk

Actual Golang support for FVM while retaining support for TinyGo at the same time

**Assumptions/Requirements**:

Preconditioned by the progress of how much Go would support WASI. We could either:
- Wait for Go to support WASI
- Or support Golang through `stub` which might have an impact on performance

**Deliverables**: 
- go-fvm-sdk v0.x
- Performance metrics (WASM target size, memory usage, time usage) of Go Vs. TinyGo
- Updated CI workflows
- Update Document for golang

**Funding for this Milestone**:

**Estimated Milestone Delivery**:

Three month. (End of Feb 22)


## Total Budget Requested

<!--Sum up the total requested budget across all milestones, and include that figure here. Also, please include a budget breakdown to specify how you are planning to spend these funds. -->

## Maintenance and Upgrade Plans

<!-- Specify your team's long-term plans to maintain this software and upgrade it over time. -->

The team is willing to continue the development of this RFP after M4. Another evaluation will be needed at then to further the planning.

## Team Members

<!-- - Team Member 1 -->
<!-- - Team Member 2 -->
<!-- - Team Member 3 -->
<!-- - ...

## Team Member LinkedIn Profiles

<!-- - Team Member 1 LinkedIn profile -->
<!-- - Team Member 2 LinkedIn profile -->
<!-- - Team Member 3 LinkedIn profile -->


## Team Website

https://forcecommunity.io/

## Relevant Experience

Force community has been an active contributor to Web3 ecosystem and Filecoin ecosystem in general. The engineering team from Force community has a track record of contributing code to Lotus as far back as Testnet and Space Race. 

## Team code repositories

https://github.com/ipfs-force-community

## Additional information

Force community is committed to become a major contributor to Web3 infrastructure and we see Filecoin at the core of the big Web3 migration. We hope that we could fast track the realization of Web3 adoption by contributing our software development capacity to the course and join hand in hand with all other ecosystem developers around the globe through this historical journey!