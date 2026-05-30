# Supply Chain & Operations – Incident Management System Architecture
1. Solution Overview
This project implements an AI-driven Incident Management workflow for Supply Chain and Operations using a multi-agent architecture built with CrewAI and OpenAI LLMs.
The system automates operational incident handling by using specialized AI agents that collaborate sequentially to:
- Understand incident reports
- Classify operational issues
- Analyze SLA/business impact
- Recommend corrective actions
- Determine escalation priority
The workflow is orchestrated using CrewAI, where each agent performs a dedicated operational responsibility.
2. High-Level Workflow
Incident Input
↓
Incident Identification Specialist
↓
Operation SLA Reasoning Specialist
↓
Action Recommendation Specialist
↓
Escalation Priority Decision Agent
↓
Final Consolidated Response
3. Technology Stack
- CrewAI
- OpenAI GPT-4o-mini
- LangChain
- Python
- dotenv
- Jupyter Notebook
4. Core Architecture Components
LLM Layer
The notebook initializes the OpenAI model using:
llm = ChatOpenAI(model="gpt-4o-mini", temperature=0)
Purpose:
- Natural language understanding
- Operational reasoning
- Incident interpretation
- Recommendation generation
Temperature=0 ensures:
- Deterministic outputs
- Stable operational decisions
- Consistent incident classification
5. Multi-Agent Architecture
5.1 Incident Identification Specialist
Responsibilities:
- Detect incident type
- Determine urgency
- Assess customer impact
Example detections:
- Shipment delays
- Inventory mismatches
- Vendor issues
- Process failures
5.2 Operation SLA Reasoning Specialist
Responsibilities:
- Analyze SLA implications
- Evaluate operational impact
- Assess business severity
5.3 Action Recommendation Specialist
Responsibilities:
- Suggest corrective actions
- Recommend operational recovery
- Provide mitigation guidance
Example actions:
- Warehouse audit
- Vendor escalation
- Replacement shipment
5.4 Escalation Priority Decision Agent
Responsibilities:
- Determine escalation severity
- Decide operational priority
- Recommend escalation level
6. CrewAI Orchestration Flow
CrewAI orchestrates sequential task execution:
Task 1 → Identify Incident
Task 2 → SLA Reasoning
Task 3 → Action Recommendation
Task 4 → Escalation Evaluation
Final AI-generated response is consolidated from all agent outputs.
7. Design Principles Used
- Modular Agent Design
- Separation of Concerns
- Single Responsibility Principle
- Extensibility
- Reusability
