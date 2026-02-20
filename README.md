# TypeScript Best Practices

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Skills](https://img.shields.io/badge/skills.sh-typescript--best--practices-blue)](https://skills.sh/ofershap/typescript-best-practices)

Modern TypeScript 5.x patterns your AI agent should use. Strict mode, discriminated unions,
`satisfies` operator, const assertions, branded types, `NoInfer`, `using`, and type-safe patterns.

> AI coding assistants default to `any`, skip strict mode, use `as` instead of `satisfies`, and
> model states with optional fields instead of discriminated unions. This plugin enforces the
> patterns that make TypeScript worth using.

## Install

### Cursor / Claude Code / Windsurf

```bash
npx skills add ofershap/typescript-best-practices
```

Or copy `skills/` into your `.cursor/skills/` or `.claude/skills/` directory.

## What's Included

| Type    | Name                        | Description                                                                                 |
| ------- | --------------------------- | ------------------------------------------------------------------------------------------- |
| Skill   | `typescript-best-practices` | 13 rules for strict mode, satisfies, discriminated unions, branded types, NoInfer, and more |
| Rule    | `best-practices`            | Always-on behavioral rule that enforces current TypeScript patterns                         |
| Command | `/audit`                    | Scan your codebase for TypeScript anti-patterns                                             |

## What Agents Get Wrong

| What the agent writes                | What you should use                                  |
| ------------------------------------ | ---------------------------------------------------- |
| `any` for uncertain types            | `unknown` with type narrowing                        |
| `as SomeType` to silence errors      | `satisfies SomeType` for validation without widening |
| `{ success?: Data; error?: string }` | Discriminated union with `type` field                |
| `strict: false` in tsconfig          | `strict: true` with proper null handling             |
| `import { SomeType }`                | `import type { SomeType }` for type-only imports     |
| `TypeVar` + `Generic[T]` patterns    | `NoInfer<T>`, const assertions, branded types        |

## Related Plugins

- [tailwind-best-practices](https://github.com/ofershap/tailwind-best-practices) - Tailwind CSS v4
  patterns
- [drizzle-best-practices](https://github.com/ofershap/drizzle-best-practices) - Type-safe Drizzle
  ORM patterns
- [python-best-practices](https://github.com/ofershap/python-best-practices) - Modern Python 3.12+
  type hints and patterns

## Author

[![Made by ofershap](https://gitshow.dev/api/card/ofershap)](https://gitshow.dev/ofershap)

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=flat&logo=linkedin&logoColor=white)](https://linkedin.com/in/ofershap)
[![GitHub](https://img.shields.io/badge/GitHub-Follow-181717?style=flat&logo=github&logoColor=white)](https://github.com/ofershap)

## License

MIT
