# Patterns Directory

This directory contains discovered development patterns and anti-patterns organized by technology stack and use case.

## Structure

```
patterns/
├── frameworks/           # Framework-specific patterns
│   ├── astro/           # Astro.js patterns
│   ├── react/           # React patterns
│   └── vue/             # Vue.js patterns
├── deployment/          # Deployment patterns
│   ├── cloudflare/      # Cloudflare Workers patterns
│   ├── vercel/          # Vercel deployment patterns
│   └── aws/             # AWS deployment patterns
├── common-mistakes/     # Frequently detected anti-patterns
├── best-practices/      # Proven best practices
└── architecture/        # Architecture patterns
```

## Pattern Schema

Each pattern should follow this structure:

```json
{
  "id": "unique-pattern-id",
  "type": "pattern|anti-pattern",
  "category": "framework|deployment|architecture",
  "stack": ["astro", "cloudflare"],
  "description": "Clear description of the pattern",
  "detection": {
    "regex": "pattern to detect",
    "context": ["file types", "locations"]
  },
  "correction": {
    "replace": "old pattern",
    "with": "new pattern",
    "reason": "why this correction works"
  },
  "documentation": {
    "source": "https://docs.example.com",
    "lastVerified": "2024-01-01"
  },
  "confidence": 0.95,
  "metadata": {
    "discoveredBy": "agent-id",
    "validatedCount": 42,
    "lastUpdated": "2024-01-01T00:00:00Z"
  }
}
```

## Adding Patterns

Patterns are automatically added by EDAT agents through the knowledge-writer service. Manual additions should validate against live documentation.