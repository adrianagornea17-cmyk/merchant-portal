---
name: jira-story
description: Use whenever creating a new Jira story/issue (via jira_create_issue or by drafting text for the user to paste into Jira). Enforces a fixed structure — Description (user story + why), Acceptance Criteria, Links — so every story is written consistently. Trigger on "create a jira story/ticket", "log a jira issue", "write up a ticket for this", etc.
---

# Jira story structure

Every Jira story created for this project (mockups/merchant-portal work, project **ET**) must follow this structure in the issue description field. Do not skip a section — if a section genuinely has nothing to add (e.g. no links yet), keep the heading and write "N/A" rather than omitting it.

## 1. Description
Two parts, in order:

1. **User story** in the classic form:
   > As a `<role>`, I want `<capability>`, so that `<benefit>`.
2. A short paragraph (1-4 sentences) giving the *why* — the context or problem driving the change. Pull this from what the user tells you; don't invent motivation.

## 2. Acceptance Criteria
A bullet list covering every concrete, testable rule implied by the request: UI updates, business rules, validations, edge cases, error states. Each bullet should be a single verifiable statement (Given/When/Then is fine but not required). Do not write vague criteria like "works correctly" — make each one checkable.

## 3. Links
A bullet list of supporting references: mockup files (link to the relevant `.html` in this repo, or the live GitHub Pages URL — see CLAUDE.md for the base URL), Figma frames, related tickets, screenshots. If none exist yet, write "N/A" — don't drop the section.

## Template to fill in

```
h2. Description

As a [role], I want [goal], so that [reason].

[1-4 sentences of context: why this change is needed.]

h2. Acceptance Criteria
* [criterion 1]
* [criterion 2]
* [criterion 3]

h2. Links
* [mockup / Figma / related ticket link, or "N/A"]
```

(Use `h2.` Jira wiki markup if creating via the REST API/MCP tool with a wiki-style description field; use plain `##` Markdown headings if the target field renders Markdown instead.)

## When actually filing the ticket via the Jira MCP tool
- Project key is **ET** unless the user says otherwise (see project reference memory for fixVersion naming and custom field IDs).
- Put the full templated text above into the `description` field.
- Set `summary` to a short, specific title (not "Fix bug" — name the actual change).
- If the user mentions a mockup file in this repo or a live URL, resolve it to the actual `.html` file / GitHub Pages link and put it under Links.

## When just drafting text (no MCP call)
Output the filled-in template directly so the user can paste it into Jira. Ask the user for anything you don't have (role, benefit, criteria, links) rather than inventing placeholder content — except you may propose draft acceptance criteria based on the request for the user to confirm/edit.
