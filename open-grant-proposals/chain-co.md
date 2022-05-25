# Grant Proposal: `A high availability solution for Filecoin Daemon`

**Name of Project: Chain-co**

**Proposal Category:** `core-dev`

<!-- grants分类https://github.com/filecoin-project/devgrants/tree/master/open-grants -->

**Proposer:** `replace with your GitHub username`

**(Optional) Technical Sponsor:** N/A

**Do you agree to open source all work you do on behalf of this RFP and dual-license under MIT and APACHE2 licenses?:** Yes

# Project Description

<!-- Please describe exactly what you are planning to build. Make sure to include the following: -->
<!-- - Start with the need or problem you are trying to solve with this project. -->
<!-- - Describe why your solution is going to adequately solve this problem. -->

At the time of writting this proposal, Filecoin network has reached ~16 EiB storage power with ~20 to ~30 PiB growth per day. Given that more than 400 nodes are having 10+ PiB of storage power with top nodes even having 100+ PiB storage power, a high availability solution for Filecoin daemon would be crucial to the stability and overall health of the network. Imagine the Filecoin daemon node for a 100 PiB storage system failed to sync height with network or experienced severe hardware failure for an extended period of time, storage power would be wiped out and causing turbulence to the network, which is not ideal at all.

In order to mitigate the risk of Filecoin daemon failure and to secure a generally sane and coherent network, we propose chain coordination, chain-co for short, to coordinate a collection of redundant daemon nodes and let the storage system to use the daemon that has the most height synced. Thus, paves the way for a stronger and more resilient Filecoin network.

<!-- This section should be 2-3 paragraphs long. -->

## Value

<!-- Please describe in more detail why this proposal is valuable for the Filecoin ecosystem. Answer the following questions: -->
<!-- - What are the benefits to getting this right? -->

The benefits of chain-co to the long-term health of Filecoin infrastructure is profound. For storage providers, they can now rest assure that there wouldn’t be a single point of failure for their storage systems. For ecosystem partners, they can now build upon a more reliable infrastructure for their applications. For end storage user, they can also enjoy a more consistent storage service without denials. Imagine an ideal world that each of the four filecoin implementation represents 25% of the network and chain-co have a collection redundancy daemons of the four implememntations. In case when one implementation fails to sync, chain-co solution could help to make sure that the Filecoin network wouldn’t suffer denial of service.

<!-- - What are the risks if you don't get it right? -->

On the other hand, the risk of not having chain-co infrastructure would deprive storage providers, ecosystem partners and end storage user the exact benefits described above, which also represent a systemic risk that the whole Filecoin network come into a halt if one implementation of the Filecoin fail to sync. 

<!-- - What are the risks that will make executing on this project difficult? -->

<!-- This section should be 1-3 paragraphs long. -->

## Deliverables

<!-- Please describe in details what your final deliverable for this project will be. Include a specification of the project and what functionality the software will deliver when it is finished. -->

Chain-co solution will be running in between a pool of redundant Fileccoin daemon of different flavors and a proxy agent. 

![arch](https://raw.githubusercontent.com/hunjixin/imgpool/master/chain-co.png)

- Filecoin daemon support: Lotus, Venus, Forest, Fuhon
- Proxy agent support: Nginx, SLB (on demand if there are popular community requests)
- Main function to coordinate between a pool of redundancy daemon nodes and return one with largest height
- A light weight HA solution for chain-co itself
- CLI for RPC, RPC client, run
- Documentations

## Development Roadmap

<!-- Please break up your development work into a clear set of milestones. This section needs to be very detailed (will vary on the project, but aim for around 2 pages for this section). -->

<!-- For each milestone, please describe: -->
<!-- - The software functionality that we can expect after the completion of each milestone. This should be detailed enough that it can be used to ensure that the software meets the specification you outlined in the Deliverables. -->
<!-- - How many people will be working on each milestone and their roles -->
<!-- - The amount of funding required for each milestone -->
<!-- - How much time this milestone will take to achieve (using real dates) -->

## Total Budget Requested

<!--Sum up the total requested budget across all milestones, and include that figure here. Also, please include a budget breakdown to specify how you are planning to spend these funds. -->

## Maintenance and Upgrade Plans

<!-- Specify your team's long-term plans to maintain this software and upgrade it over time. -->

Chain-co will be committed to integrate the daemons of all four implementation of Filecoin to offer community a complete the high availability solution.

# Team

## Team Members

<!-- - Team Member 1 -->
<!-- - Team Member 2 -->
<!-- - Team Member 3 -->
<!-- - ...

## Team Member LinkedIn Profiles

<!-- - Team Member 1 LinkedIn profile -->
<!-- - Team Member 2 LinkedIn profile -->
<!-- - Team Member 3 LinkedIn profile -->
<!-- - ...

## Team Website

https://forcecommunity.io/

<!-- Please link to your team's website here (make sure it's `https`) -->

## Relevant Experience

<!-- Please describe (in words) your team's relevant experience, and why you think you are the right team to build this project. You can cite your team's prior experience in similar domains, doing similar dev work, individual team members' backgrounds, etc. -->

Force community has been an active contributor to Web3 ecosystem and Filecoin ecosystem in general. The engineering team from Force community has a track record of contributing code to Lotus as far back as Testnet and Space Race. 

## Team code repositories

<!-- Please provide links to your team's prior code repos for similar or related projects. -->

# Additional Information

<!-- Please include any additional information that you think would be useful in helping us to evaluate your proposal. -->
