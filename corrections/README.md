# Corrections Directory

This directory contains recorded corrections from AI suggestion failures, organized by the type of mistake and the stack involved.

## Structure

```
corrections/
├── training-cutoff/     # Issues from outdated training data
├── syntax-errors/       # Code syntax mistakes
├── version-mismatches/  # Framework version incompatibilities  
├── configuration/       # Config file errors
└── integration/         # Service integration issues
```

## Correction Schema

Each correction record should follow this structure:

```json
{
  "id": "correction-id",
  "timestamp": "2024-01-01T00:00:00Z",
  "context": {
    "agent": "claude-4.0",
    "project": "project-name",
    "stack": ["astro", "cloudflare"],
    "file": "relative/path/to/file.ts",
    "operation": "implementation|debugging|configuration"
  },
  "failure": {
    "category": "training-cutoff|syntax|version-mismatch|config|integration",
    "aiSuggestion": "The suggestion that failed",
    "error": "The error that occurred",
    "symptoms": ["observable symptoms"]
  },
  "correction": {
    "workingCode": "The code that actually works",
    "explanation": "Why this works instead",
    "source": "https://docs.example.com/correct-way",
    "confidence": 0.98
  },
  "prevention": {
    "detectionPattern": "regex or rule to catch this",
    "validationRule": "how to validate the fix",
    "documentationCheck": "which docs to verify against"
  },
  "impact": {
    "timeWasted": "30 minutes",
    "similarCases": 15,
    "preventedBy": "edat-validation"
  }
}
```

## Usage

Corrections are used to:
- Train pattern detection systems
- Prevent repeated mistakes
- Update validation rules
- Improve AI suggestions
- Build knowledge for future agents

## Recording Corrections

Corrections are automatically recorded when:
1. An AI suggestion fails to work
2. A human developer fixes the issue
3. The fix is validated and confirmed
4. The learning is shared across the EDAT network