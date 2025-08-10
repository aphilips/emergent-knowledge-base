# Learnings Directory

This directory contains agent learnings and insights from development sessions, organized chronologically and by agent type.

## Structure

```
learnings/
├── session-summaries/   # Daily/session learning summaries
├── corrections/         # Specific correction learnings
├── insights/           # General development insights
└── validations/        # Pattern validation results
```

## Learning Schema

Each learning record should follow this structure:

```json
{
  "id": "learning-id",
  "timestamp": "2024-01-01T00:00:00Z",
  "agent": {
    "type": "claude|gpt-4|cursor|copilot",
    "version": "4.0",
    "session": "session-id"
  },
  "context": {
    "project": "project-name",
    "stack": ["astro", "cloudflare"],
    "operation": "debugging|implementation|review"
  },
  "learning": {
    "category": "pattern|correction|insight|validation",
    "description": "What was learned",
    "trigger": "What caused this learning",
    "outcome": "What was the result"
  },
  "impact": {
    "severity": "critical|high|medium|low",
    "scope": "project|stack|global",
    "confidence": 0.95
  },
  "metadata": {
    "validated": true,
    "sharedWith": ["other-agents"],
    "appliedCount": 5
  }
}
```

## Usage

Learnings are automatically collected by EDAT agents and used for:
- Improving pattern detection
- Training future suggestions
- Building collective intelligence
- Preventing repeated mistakes