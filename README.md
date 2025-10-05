# Blog:  ChatGPT Prompt Interface Command Reference
Published:  2025-10-05

This document provides a list of **command-style instructions** that can be entered directly in the ChatGPT prompt interface to control behavior, formatting, and response style.  
These are **user-facing directives**, not programming commands — they guide how ChatGPT should interpret and respond to your input.

---

## 🧭 General Control Commands

| **Command** | **Description** | **Example Usage** |
|--------------|------------------|--------------------|
| `temperature=<value>` | Adjusts creativity vs. precision of responses. Lower = factual, higher = creative. | `temperature=0.2` (precise) / `temperature=1.2` (creative) |
| `format=markdown` | Forces responses to be formatted using Markdown syntax. | `format=markdown` |
| `format=default` | Returns formatting to plain text. | `format=default` |
| `role=<description>` | Assigns ChatGPT a role or persona for context-specific responses. | `role: you are a cybersecurity analyst providing incident summaries.` |
| `context:` | Provides background information or scenario context for the current prompt. | `context: you are assisting a global IT team during an AI rollout.` |
| `objective:` | Defines the goal or deliverable expected from ChatGPT. | `objective: write a 500-word briefing for executives.` |
| `tone=<descriptor>` | Sets the tone or style of the response. | `tone=formal`, `tone=analytical`, `tone=creative` |
| `limit=<number>` | Requests a specific word or sentence limit. | `limit=250 words` |
| `reset` | Clears previous contextual assumptions (role, temperature, format, etc.). | `reset` |

---

## 🗂️ Structural and Output Commands

| **Command** | **Purpose** | **Example** |
|--------------|-------------|--------------|
| `format=table` | Requests information to be presented as a Markdown table. | `format=table` |
| `format=codeblock` | Outputs text within code block formatting (useful for Markdown, JSON, or Python). | `format=codeblock` |
| `summarize:` | Asks ChatGPT to condense provided content or conversation into a summary. | `summarize: the following project notes` |
| `rewrite:` | Instructs ChatGPT to rephrase or refine text while retaining meaning. | `rewrite: make this more concise and professional` |
| `explain:` | Requests a clear, beginner-friendly explanation of a term or concept. | `explain: zero trust architecture` |
| `compare:` | Asks for differences or similarities between two items. | `compare: cloud-native vs. on-premise systems` |
| `generate:` | Signals that ChatGPT should produce or create original content. | `generate: a short story set in a futuristic data center` |

---

## ⚙️ Session Management Commands

| **Command** | **Function** | **Example** |
|--------------|--------------|--------------|
| `acknowledge` | Requests explicit confirmation that ChatGPT has understood your instructions. | `acknowledge` |
| `baseline` | Sets the current configuration or document as a baseline for future reference. | `baseline: this version of the report is final` |
| `new baseline` | Replaces the previously stored baseline with updated instructions or content. | `new baseline` |
| `pause` | Pauses action or generation (conceptually acknowledged). | `pause` |
| `continue` | Resumes the next step or section. | `continue` |
| `show current settings` | Displays current temperature, formatting, and role. | `show current settings` |

---

## 🧩 Example Prompt Composition

temperature=0.7
format=markdown
role: you are a technical writer summarizing IT incidents.
context: summarizing an outage postmortem for executives.
objective: produce a concise, factual report in 250 words.
tone=formal
acknowledge.


---

## 🔒 Notes and Best Practices

- Commands should be placed **at the top of your prompt** for clarity.  
- Each command can be combined in a single prompt (ChatGPT interprets them in sequence).  
- Always specify the **objective** and **context** to improve accuracy.  
- Use `temperature=0.2` for analytical or compliance work and `temperature=1.0+` for brainstorming or storytelling.

---

© 2025 Brock Frary. All rights reserved.
