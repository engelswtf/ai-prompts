# Contributing to AI Prompts

Thank you for your interest in contributing! This document provides guidelines for adding new prompts or agents to the collection.

## Types of Contributions

### 1. New Prompts
Add new micro-prompts to existing packs or propose new packs.

### 2. New Agents
Add new specialized agent configurations.

### 3. Improvements
Enhance existing prompts with better examples, clearer instructions, or additional model compatibility.

### 4. Bug Fixes
Fix issues with existing prompts that produce inconsistent results.

## Prompt Format

All prompts must follow this format:

```yaml
---
id: unique-kebab-case-id
name: Human Readable Name
version: "1.0.0"
author: your-name-or-handle
license: MIT
category: existing-category
tags: [relevant, tags, here]
model_compatibility: [claude, gpt-4, gemini, llama]
---

# Prompt Title

## Role
Describe the expert persona the AI should adopt. Be specific about:
- Years of experience
- Domain expertise
- Key skills

## Task
Clearly state what the AI should do:
1. Primary objective
2. Secondary objectives
3. Expected deliverables

## Input
Define the input format with placeholders:

```
{{variable_name}}
```

## Output Format
Specify exactly what the output should look like:
- Structure
- Sections
- Tables or lists

## Constraints

### DO
- Positive behaviors to enforce

### DO NOT
- Negative behaviors to prevent

## Examples

### Example 1: [Scenario Name]

**Input:**
```
[Example input]
```

**Output:**
```
[Example output]
```
```

## Quality Checklist

Before submitting, verify:

- [ ] Prompt follows the standard format
- [ ] ID is unique and kebab-case
- [ ] Category matches an existing pack (or propose new)
- [ ] Tags are relevant and lowercase
- [ ] Tested with at least 2 AI models
- [ ] Examples are realistic and helpful
- [ ] Constraints are specific (not vague)
- [ ] No hardcoded values that should be variables

## Testing Your Prompt

1. **Test with Claude Sonnet** - Primary target model
2. **Test with GPT-4** - Verify cross-model compatibility
3. **Test edge cases** - Empty inputs, malformed data, etc.
4. **Verify output consistency** - Run 3+ times, results should be similar

## Submitting Changes

1. Fork the repository
2. Create a feature branch: `git checkout -b add-new-prompt`
3. Add your prompt to the appropriate directory
4. Update the pack's README if adding a new prompt
5. Commit with a clear message: `git commit -m "Add memory-profiler prompt to debugging pack"`
6. Push and create a Pull Request

## Pull Request Template

```markdown
## What does this PR add?
[Brief description]

## Category
[Which pack does this belong to?]

## Testing
- [ ] Tested with Claude
- [ ] Tested with GPT-4
- [ ] Verified output consistency
- [ ] Tested edge cases

## Example Output
[Show a real example of the prompt working]
```

## Code of Conduct

- Be respectful and constructive
- Focus on improving the collection
- Credit sources and inspirations
- Keep discussions technical and productive

## Questions?

Open an issue or reach out via the website: [engels.wtf/contact](https://www.engels.wtf/contact)
