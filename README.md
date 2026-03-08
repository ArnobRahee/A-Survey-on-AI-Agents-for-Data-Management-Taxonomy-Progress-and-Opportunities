# AI Agents for Data Management

**A Survey on AI Agents for Data Management: Taxonomy, Systems, and Future Directions**

This repository accompanies our survey paper on the emerging intersection of **AI agents and data management systems**. Recent advances in **large language models (LLMs)** have enabled autonomous agents capable of reasoning, planning, and interacting with external tools, opening new possibilities for automating complex data workflows.

The goal of this survey is to **systematically analyze how LLM-based agents are being applied to core data management tasks**, and to provide a **unified taxonomy of agentic architectures, capabilities, and system designs**.

---

# Overview

Traditional data management systems rely on manually designed pipelines, rule-based scripts, and query optimization techniques. With the emergence of **LLM-powered agents**, many of these workflows can now be automated through natural language instructions combined with reasoning, planning, and tool execution.

This survey studies how agentic systems support tasks such as:

- Data cleaning
- Data integration
- ETL pipeline automation
- Query generation
- Database administration
- Data validation
- Data analysis

The paper provides a **comprehensive overview of the architectural patterns and design principles** behind these systems.

---

# Survey Contributions

## 1. Unified Taxonomy of Agentic Systems

We introduce a taxonomy for analyzing AI agents in data management based on:

- **Agent architecture** (single-agent vs multi-agent)
- **Orchestration strategies**
- **Planning mechanisms**
- **Memory systems**
- **External tool integration**
- **Supported data modalities**

This taxonomy helps organize a rapidly growing ecosystem of LLM-based agent frameworks.

---

## 2. Systematic Review of Existing Systems

The survey analyzes several emerging systems that apply LLM agents to data workflows, including:

- CleanAgent
- DocETL
- InsightPilot
- WaitGPT
- Jupybara
- DataGovAgent
- other recent LLM-based agent frameworks

Each system is evaluated based on:

- orchestration model
- planning capability
- memory mechanisms
- scalability
- tool usage
- supported data types

---

## 3. Data Lifecycle Perspective

We study how agentic systems operate across the **entire data lifecycle**.

| Data Management Task | Description |
|---------------------|-------------|
| Data Cleaning | Detecting and repairing data errors |
| Data Integration | Schema matching and entity resolution |
| ETL Automation | Data transformation pipelines |
| Query Optimization | Improving database performance |
| Database Administration | Autonomous system tuning |
| Data Validation | Ensuring correctness and consistency |

---

## 4. Agentic Workflow Architecture

Most agentic systems for data management follow a common architectural workflow that combines **LLM reasoning with external data tools and execution environments**.

Unlike traditional data pipelines, these systems rely on an **LLM-driven control loop** where the agent interprets user instructions, generates plans, invokes tools, and iteratively refines its outputs.

A typical workflow consists of the following stages:

### 1. User Instruction
The process begins with a natural language instruction from the user.  
This instruction may request tasks such as:

- cleaning a dataset
- generating SQL queries
- building ETL pipelines
- validating data quality
- performing exploratory data analysis

The instruction is provided to the agent along with relevant context such as schemas, datasets, or metadata.

---

### 2. Reasoning and Planning

The LLM agent interprets the instruction and generates a **structured plan** describing how the task should be executed.

Planning strategies used by agentic systems include:

- Chain-of-Thought reasoning
- ReAct-style reasoning and acting
- multi-step task decomposition
- iterative refinement

This planning stage determines which tools should be invoked and in what order.

---

### 3. Tool Invocation

Once a plan is produced, the agent interacts with **external tools and execution environments** to perform concrete operations.

Common tools used by agentic data systems include:

- SQL engines
- Python interpreters
- data cleaning libraries
- APIs
- database management systems
- analytics platforms

These tools allow the agent to move beyond text generation and perform **actual data operations**.

---

### 4. Memory and Context Management

Many systems maintain memory to preserve context across reasoning steps.

Memory mechanisms may include:

- conversation history
- intermediate execution results
- retrieved documents or metadata
- vector databases for long-term memory

This allows agents to maintain coherence across multi-step workflows.

---

### 5. Feedback and Iterative Execution

After executing an action, the system evaluates the output and determines whether the task has been completed successfully.

If errors are detected, the agent may:

- revise its plan
- correct generated code
- re-run queries
- refine transformations

This **closed feedback loop** enables autonomous task execution.

---

### 6. Final Output

Once the workflow converges, the system returns the final result to the user.

Outputs may include:

- cleaned datasets
- SQL queries
- analytical reports
- transformed data pipelines
- visualization outputs

---
### Unified Agentic Workflow

Although the systems covered in this survey target different data management tasks, most of them can be understood through a shared agentic pipeline. At a high level, an agent receives a user request, reasons about the task, selects appropriate tools, executes actions, and iteratively refines the result using feedback and memory.

```text
User Instruction / Task
          ↓
Task Understanding
          ↓
Reasoning & Planning
          ↓
Tool Selection and Invocation
          ↓
Execution on Data / Systems
          ↓
Memory, Context, and Intermediate State
          ↓
Feedback, Verification, and Refinement
          ↓
Final Output / Action