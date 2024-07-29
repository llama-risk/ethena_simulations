# LlamaRisk - Dashboard and Simulator for Ethena
![image](https://github.com/user-attachments/assets/8125fe96-395f-476e-93c9-9f0656a8e26b)

## 1. Executive Summary

This proposal outlines the development of a bespoke risk dashboard for Ethena, incorporating a Reserve Fund Decay Simulator. The system aims to provide comprehensive, real-time insights into Ethena's protocol health and risk metrics, offering stakeholders access to critical data and interactive analysis tools.

## 2. Objectives

- Deliver a comprehensive, real-time overview of Ethena's protocol health, risk metrics, and overall financial stability
- Enable informed decision-making through interactive simulations of various risk scenarios and their projected effects on the reserve fund
- Monitor and analyze key parameters as outlined in the internal governance document:
    - LST Allocation Range
    - CEX Allocations
    - Liquid Redemption Buffer
    - Revenue Split to reserve fund
- Track and display targets established by the risk committee

## 3. Deliverables

The proposal encompasses two primary components:

1. A risk and metrics dashboard
2. Interactive simulators focused on the reserve fund, enabling users to test various risk assumptions

### Dashboard

The following is a non-exhaustive list of proposed sections and visualizations for inclusion in the dashboard:

1. Protocol key metrics (supplementing those covered by the [Ethena dashboard](https://app.ethena.fi/dashboards/solvency))
2. Current metrics vs. risk committee targets monitoring (comparable to the [Aave GHO dashboard](https://aave.tokenlogic.xyz/liquidity-committee))
3. Reserve fund breakdown over time
4. USDe and sUSDe liquidity analysis (aggregated and detailed, covering multiple venues)
5. sUSDe peg monitoring
6. Weekly protocol performance (LST + perpetual funding rates)
7. Treasury composition
8. Month-over-month custodian attestations (cf. [mirror.xyz](https://mirror.xyz/0xF99d0E4E3435cc9C9868D1C6274DfaB3e2721341/bwzBngcOk-n9XB0venIjS1OPiSx3-39GDcqUaOABpgM))
9. sUSDe exit queue status
10. Whitelisted users for minting/redemption of USDe
11. Timelock monitoring

This list may be modified based on the requirements of the Ethena team.

### Reserve Fund Simulators

The interactive sections will feature simulators designed to estimate the decay and replenishment of Ethena's reserve fund under various scenarios. These tools will utilize real-time data on Ethena's Total Value Locked (TVL), insurance fund size, and other relevant metrics. The simulators will allow users to input their assumptions and perform risk-based calculations interactively. This functionality will build upon the following proof of concept:


![image](https://github.com/user-attachments/assets/7f93e08d-26c9-4a7b-8155-ff9af1e3d236)
[Proof of Concept by LlamaRisk - Desmos playground](https://www.desmos.com/calculator/zwaetu7xlu)

![image](https://github.com/user-attachments/assets/ef1ab929-0242-41b7-b89d-d7d886e93d5a)
[Proof of Concept Reserve Fund Decay Simulator](https://codepen.io/rfyfvrfm-the-bold/pen/KKjPVqm)

Additional parameters and controls will be implemented to simulate various market conditions.

## 4. Technical Implementation

The dashboard and simulator will be hosted and maintained by LlamaRisk. The proposed technical stack includes:
- Backend: Django (Python), PostgreSQL, Redis
- Frontend: Next.js, React

## 5. Timeline

The project will be structured in phases, with regular weekly or bi-weekly meetings scheduled with the Ethena team to ensure alignment, address challenges, and incorporate iterative feedback.

- Phase 0: Scope Finalization (1 week)
- Phase 1: Planning, Conceptualization, and Design (2 weeks)
- Phase 2: Core Development (6 weeks)
- Phase 3: Frontend Development and Integration (4 weeks)
- Phase 4: Testing and Refinement (1 week)
- Phase 5: Deployment and Documentation (1 week)

Total projected timeline: 15 weeks
