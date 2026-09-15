# Anthropic Claude Certified Architect Foundations (CCAR-F) Exam Preparation 2026

This repository provides study material and practice questions for the **Anthropic Claude Certified Architect Foundations (CCAR-F)** certification. It is intended for learners preparing for **Anthropic exam prep**, Claude architecture concepts, and **AI architect certification**.

The practice questions below cover areas such as Claude Agent SDK, Model Context Protocol (MCP), tool use, escalation strategies, error handling, Claude Code, and automated code review.

**CCAR-F Preparation Resources:**
https://www.skillcertexams.com/anthropic/ccar-f-dumps.html

## CCAR-F Practice Questions

### Question 1

You are building a customer support resolution agent using the Claude Agent SDK. The agent uses MCP tools such as `get_customer`, `lookup_order`, `process_refund`, and `escalate_to_human`. A tool currently returns only the generic error message "Tool execution failed." What change would give Claude enough information to select an appropriate recovery action?

* A. Hide all errors and retry them inside the tool.
* B. Return error-specific messages explaining what went wrong and what Claude should try next.
* C. Remove the error flag and return all failures as normal tool content.
* D. Replace Claude's reasoning with hardcoded retry and escalation logic.

**Answer: B**

### Question 2

A customer says, "This is frustrating. I want to talk to a real person NOW." The agent has not yet investigated the customer's account. What should the agent do?

* A. Continue troubleshooting and escalate only if the customer repeats the request.
* B. Call account and order tools first, then escalate.
* C. Immediately call the human escalation tool.
* D. Acknowledge the customer's frustration and ask a targeted question before escalating.

**Answer: C**

### Question 3

Which approach is most reliable for identifying situations that genuinely require human intervention?

* A. Use a fixed rules engine for every issue type.
* B. Instruct the agent to escalate for human requests, policy exceptions, or situations where it cannot make meaningful progress.
* C. Escalate after exactly three unsuccessful tool calls.
* D. Escalate whenever sentiment analysis detects frustration.

**Answer: B**

### Question 4

After `lookup_order` returns order details showing that an item was purchased 45 days ago, how does the agentic loop determine whether to call `process_refund` or `escalate_to_human`?

* A. The order details are added to the conversation and the model reasons about the next action.
* B. The orchestration layer automatically selects the next tool.
* C. A fixed decision tree selects the next tool.
* D. The agent follows a tool sequence created at the beginning.

**Answer: A**

### Question 5

An agent sometimes reaches its `max_turns` limit after gathering information but before resolving the customer's issue. How can the system guarantee that the interaction ends with either a resolution or human handoff?

* A. Automatically escalate when 80% of the turn budget is reached.
* B. Split the process between two separate agents.
* C. Have the orchestration layer check the final outcome and programmatically escalate if neither resolution nor escalation occurred.
* D. Add stronger system-prompt instructions.

**Answer: C**

### Question 6

A company requires every refund above $500 to be escalated to a human. Prompt instructions alone have resulted in occasional policy violations. What provides the strongest enforcement?

* A. Add more examples to the prompt.
* B. Use stronger wording in the system prompt.
* C. Make the refund tool reject transactions above the threshold.
* D. Intercept the tool call with a hook, block the refund, and trigger human escalation.

**Answer: D**

### Question 7

During a billing dispute, the agent verifies the customer and refund eligibility, but `process_refund` returns a timeout. What is the best response?

* A. Retry indefinitely until the refund succeeds.
* B. Tell the customer the refund will be processed and close the conversation.
* C. Explain the billing information, confirm eligibility, acknowledge the system problem, and offer escalation or a later retry.
* D. Immediately escalate without explaining the situation.

**Answer: C**

### Question 8

An agent discovers that a promotional pricing issue requires manager approval beyond its authorization level. What is the best escalation approach?

* A. Send only the customer's original message.
* B. Create a structured handoff containing customer details, order information, and the identified issue.
* C. Attempt the refund anyway.
* D. Save the entire conversation to a database and send only a reference ID.

**Answer: B**

### Question 9

When using Claude Code to locate every occurrence of a dangerous function such as `eval()` across a large codebase, which tool is most appropriate for content searching?

* A. Glob
* B. Grep
* C. Read
* D. Bash with `ls -R`

**Answer: B**

### Question 10

An automated reviewer has strong recall for API design but poor recall for business-logic bugs. Adding business-logic examples improves logic recall but causes API recall to decline. What is the best approach?

* A. Provide the entire repository as context.
* B. Replace examples with a long checklist.
* C. Split the review into focused prompts for different concern categories and consolidate the findings.
* D. Upgrade to a more capable model.

**Answer: C**

### Question 11

A Claude Code review repeatedly flags project patterns that are intentionally accepted by the development team. Which approach supplies these conventions as persistent context for every review?

* A. Document accepted patterns in the project's `CLAUDE.md` file.
* B. Review only changed lines.
* C. Filter findings afterward with keywords.
* D. Add suppression comments to every affected line.

**Answer: A**

### Question 12

An automated code reviewer has high precision but low recall because its prompt says to report only issues it is highly confident about. What approach can substantially improve bug detection while maintaining a manageable false-positive rate?

* A. Add examples while keeping the conservative instruction unchanged.
* B. Remove all conservative instructions and report everything.
* C. Use a broad finding stage followed by a separate verification and thresholding stage.
* D. Add more repository context without changing the review process.

**Answer: C**

### Question 13

Developers report many false positives from an automated code review system. The goal is to help the model distinguish acceptable project-specific patterns from genuine issues and still generalize to new situations. What is most effective?

* A. List every pattern that should never be flagged.
* B. Provide annotated examples showing acceptable patterns versus genuine issues.
* C. Remove findings using keyword filters.
* D. Tell Claude to report only definite issues.

**Answer: B**

### Question 14

A pull-request review receives only changed files and repeatedly misses bugs involving unchanged files, such as callers still using an old function parameter order. What is the most effective design change?

* A. Include every file within two dependency hops.
* B. Tell the model to reason about unseen callers.
* C. Redesign the review as a turn-limited agentic task that can search and read the repository as needed.
* D. Run a separate review for every changed file.

**Answer: C**

### Question 15

A development team has accepted patterns that an automated reviewer repeatedly flags, including force-unwrapping in test files, large coordinator classes, and internally maintained deprecated modules. What should be done to prevent these findings?

* A. Filter the findings afterward with keywords.
* B. Limit the review to changed lines.
* C. Use inline suppression comments.
* D. Document the team's conventions in `CLAUDE.md` so they are available during every review.

**Answer: D**

## Study Topics

The questions in this repository can help learners review:

* Anthropic Claude Certified Architect Foundations
* CCAR-F certification
* Anthropic exam preparation
* Claude Agent SDK
* Model Context Protocol (MCP)
* Claude tool use
* AI agent architecture
* Error handling and recovery
* Human escalation strategies
* Claude Code
* Automated code review
* Prompt engineering
* AI architect certification
* AI application architecture

**More CCAR-F Preparation Resources:**
https://www.skillcertexams.com/anthropic/ccar-f-dumps.html
