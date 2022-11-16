# Designing Machine Learning Projects

A template to guide the development cycle for machine learning systems that factors in product requirements, design docs and project considerations.
This template is designed to guide machine learning product development. While this template will initially be completed in sequential order, it will naturally involve nonlinear engagement based on iterative feedback. We should follow this template for every major release of our products so that all the decision making is transparent and documented.

Product (What & Why) → Engineering (How) → Project (Who & When)
While our documentation will be detailed, we can start the process by walking through a machine learning canvas: (detailed in [ml-canvas.pdf](ml-canvas.pdf))

- Background
- Value Proposition
- Objectives
- Solution
- Feasibility
- Data
- Metrics
- Evaluation
- Modeling
- Experimentation
- Feedback
- Project

From this high-level canvas, we can create detailed documentation for each release:
📂 project/
├── 📄 Overview
├── 📂 release-1
| ├── 📄 product requirements [Product]
| ├── 📄 design documentation [Engineering]
| ├── 📄 project planning [Project]
├── ...
└── 📂 release-n

## Product Management

[What & Why]: motivate the need for the product and outline the objectives and key results.

> 📝 Each section below has a dropdown component called "Our task", which will discuss the specific topic with respect to the specific product that we're trying to build.

### Background

Set the scene for what we're trying to do through a customer-centric approach:

- customer: profile of the customer we want to address
- goal: main goal for the customer
- pains: obstacles in the way of the customer achieving the goal
- gains: what would make the job easier for the customer?

### Value proposition

Propose the value we can create through a product-centric approach:

- product: what needs to be built to help the customer reach their goal?
- alleviates: how will the product reduce pains?
- advantages: how will the product create gains?

### Objectives

Breakdown the product into key objectives that we want to focus on.

### Solution

Describe the solution required to meet our objectives, including it's core features, integration, alternatives, constraints and what's out-of-scope.

May require separate documentation (wireframes, user stories, mock-ups, etc.).

### Feasibility

How feasible is our solution and do we have the required resources to deliver it (data, $, team, etc.)?

## Engineering

[How]: can we engineer our approach for building the product.

### Data

Describe the training and production (batches/streams) sources of data.

### Labeling

Describe the labeling process and how we settled on the features and labels.

### Evaluation

Before we can model our objective, we need to be able to evaluate how we’re performing.

### Modeling

While the specific methodology we employ can differ based on the problem, there are core principles we always want to follow:

- End-to-end utility: the end result from every iteration should deliver minimum end-to-end utility so that we can benchmark iterations against each other and plug-and-play with the system.
- Manual before ML: incorporate deterministic components where we define the rules before using probabilistic ones that infer rules from data → baselines.
- Augment vs. automate: allow the system to supplement the decision making process as opposed to making the final decision.
- Internal vs. external: not all early releases have to be end-user facing. We can use early versions for internal validation, feedback, data collection, etc.
- Thorough: every approach needs to be well tested (code, data + models) and evaluated, so we can objectively benchmark different approaches.

### Feedback

How do we receive feedback on our system and incorporate it into the next iteration? This can involve both human-in-the-loop feedback as well as automatic feedback via monitoring, etc.

## Project Management

[Who & When]: organizing all the product requirements into manageable timelines so we can deliver on the vision.

### Team

Which teams and specific members from those teams need to be involved in this project? It’s important to consider even the minor features so that everyone is aware of it and so we can properly scope and prioritize our timelines. Keep in mind that this isn’t the only project that people might be working on.

### Deliverables

We need to break down all the objectives for a particular release into clear deliverables that specify the deliverable, contributors, dependencies, acceptance criteria and status. This will become the granular checklist that our teams will use to decide what to prioritize.

### Timeline

This is where the project scoping begins to take place. Often, the stakeholders will have a desired time for release and the functionality to be delivered. There will be a lot of back and forth on this based on the results from the feasibility studies, so it's very important to be thorough and transparent to set expectations.
