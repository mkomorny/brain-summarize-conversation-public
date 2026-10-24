---
name: brain-summarize-conversation
description: >-
  Summarizes and writes a structured executive brief of the active conversation directly
  into your Second Brain. Extracts key objectives, accomplishments, architectural decisions,
  conventions established, and next steps, saving the brief immediately via remember.
---

# Brain Summarize Conversation (`/brain-summarize-conversation`)

Use this skill to condense your entire conversation into a senior-engineer-grade executive brief and store it as a clean, retrievable Second Brain memory.

---

## When Invoked

Direct user invocation of this command carries explicit authorization. **Execute immediately** by analyzing the conversation, synthesizing a structured brief, calling the `second-brain` MCP `remember` tool, and reporting the confirmed memory ID and saved brief.

---

## Execution Workflow

### Step 1: Synthesize the Conversation Brief
Review the conversation from start to finish and distill it into a high-density 4-part brief:
1. 🎯 **Objective**: The user's core intent, problem statement, or requested feature.
2. 🚀 **Key Accomplishments**: What was actually designed, coded, debugged, or deployed.
3. 📌 **Decisions & Conventions Locked**: Settled technical trade-offs, naming conventions, or policy rules.
4. ⏭️ **Current State & Next Steps**: What state the project/system was left in and what comes next.

### Step 2: Assign Tags and Volatility
- **Tags**: Include `#summary`, `#brief`, `#decision`, project name, and core technologies.
- **Volatility**: Default to `!durable` if permanent architectural decisions were locked, or `!state` if it reflects ongoing project status.
- **Source**: Set to `"antigravity"`, `"claude"`, or `"grok"` depending on the active platform.

### Step 3: Execute Save
Call `remember` on the `second-brain` MCP server immediately:
```json
{
  "content": "<structured executive conversation brief>",
  "tags": ["summary", "brief", "decision", ...],
  "volatility": "durable",
  "source": "antigravity"
}
```

### Step 4: Confirm
Report back:
- 🆔 **Memory ID**
- 🏷️ **Tags & Volatility**
- 📄 **Full Executive Brief**

---

## Syntax

```
/brain-summarize-conversation [optional focus or tag]
```

## Examples

```
/brain-summarize-conversation
/brain-summarize-conversation focus on UI architecture decisions
```
