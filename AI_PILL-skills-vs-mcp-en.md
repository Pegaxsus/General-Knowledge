# 💊 Information Pill — Skills vs MCP

## Key concepts

**Skills** and **MCP** are not competing approaches: they solve different problems and can be used together.

- **Skills:** teach an agent **how to perform a task** through procedures, criteria, references, and best practices.
- **MCP (Model Context Protocol):** connects an agent to **external tools and data sources** so it can retrieve information and take action.

## Skills: knowing what to do

A *Skill* packages instructions and specialized knowledge to guide task execution. It may contain:

- Step-by-step procedures.
- Best practices, methodologies, and standards.
- Templates, examples, and output formats.
- Reference documentation.

**Examples:** a penetration-testing methodology, a code-review checklist, a CIS hardening procedure, or a reporting template.

> **Skill = knowledge + methodology + working rules.**

## MCP: having the tools to act

**MCP** is a protocol for connecting AI applications to external systems and services, such as GitHub, files, APIs, or databases. Through the tools exposed by these systems, an agent can retrieve data and perform authorized operations.

> **MCP = access to tools + data + actions.**

**Analogy:** Skills provide the *know-how*, while MCP provides the *hands* needed to act.

## Combining Both

**Example: reviewing a pull request**

| Setup | Outcome |
|---|---|
| MCP only | The agent can access GitHub, read code, and post comments, but a consistent review methodology is not guaranteed. |
| Skill only | The agent knows the review procedure and security criteria, but still needs a tool to access the actual pull request. |
| Skill + MCP | The agent accesses the pull request, applies the methodology, and publishes findings through the available tools. |

**Conceptual workflow:**

```text
User → Agent (LLM) → Skill (procedure) → MCP (tools) → External system
```

This is a simplified diagram: in practice, the agent interprets the Skill instructions and decides when to invoke available tools.

## Recommended usage

| Requirement | Typical solution |
|---|---|
| Query an API or database | MCP |
| Access GitHub or interact with external services | MCP |
| Work with files or run commands through connected tools | MCP |
| Follow a methodology or standard | Skill |
| Apply specialized knowledge | Skill |
| Standardize reports and outputs | Skill |
| Execute a procedure involving external information and actions | **Skill + MCP** |

## Is a Skill just a prompt?

Not exactly. Although it relies on instructions, a Skill can bundle metadata, procedures, examples, supporting files, and reusable references. Some systems also support progressively loading this content as needed for the task.

## Practical example: a hardening agent

A local agent powered by a model such as Qwen could combine:

1. **Skill:** an Ubuntu hardening procedure based on CIS and CCN-STIC, including verification criteria and an evidence-reporting format.
2. **MCP:** tools for inspecting configuration files, executing authorized SSH commands, and accessing technical documentation.
3. **Agent:** interprets the request, applies the Skill, invokes the available tools, and collects the results.

**Result:** the agent can verify security controls using a consistent procedure, within the permissions and capabilities actually available to it.

## Conclusion (TL;DR)

**Skills define how to work; MCP enables the tools used to do the work.** Together, they help build more specialized and operationally capable agents.

---

*Reference: [Skills Directory — Skills vs MCP](https://www.skillsdirectory.com/docs/skills-vs-mcp). This is an introductory summary; the hardening example is illustrative.*
