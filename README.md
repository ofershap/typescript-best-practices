# TypeScript Best Practices

Modern TypeScript patterns your AI agent should use. Strict mode, discriminated unions, satisfies operator, const assertions, and type-safe patterns for TypeScript 5.x.

## Install

### Cursor IDE

```
/add-plugin typescript-best-practices
```

### Claude Code

```
/plugin install typescript-best-practices
```

### Skills only (any agent)

```bash
npx skills add ofershap/typescript-best-practices/typescript-best-practices
```

Or copy `skills/` into your `.cursor/skills/` or `.claude/skills/` directory.

## What's Included

### Skills

- **typescript-best-practices**  - Modern TypeScript patterns your AI agent should use. Strict mode, discriminated unions, satisfies operator, const assertions, and type-safe patterns for TypeScript 5.x.

### Rules

- **best-practices**  - Always-on rules that enforce current TypeScript patterns

### Commands

- `/audit`  - Scan your codebase for TypeScript anti-patterns

## Why This Plugin?

AI agents are trained on data that includes outdated patterns. This plugin ensures your agent uses current TypeScript best practices:

1. **Using `any` instead of `unknown`**  - Agents default to `any` when types are uncertain, opting out of type safety entirely.

2. **Skipping strict mode**  - Agents often suggest `strict: false` or omit `strictNullChecks` to avoid errors instead of fixing null/undefined handling.

3. **Type assertions over `satisfies`**  - Agents reach for `as` to silence errors, losing literal types and bypassing validation. `satisfies` checks the shape without widening.

4. **Optional fields instead of discriminated unions**  - Agents model mutually exclusive states with optional properties (success?, error?), leading to invalid combinations and weak narrowing.

5. **Ignoring new TypeScript 5.x features**  - Agents rarely use `NoInfer`, `using`, template literal types, or `noUncheckedIndexedAccess`, missing stronger type guarantees.

## License

MIT
