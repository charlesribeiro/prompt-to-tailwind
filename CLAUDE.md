# Claude AI Assistant Governance Rules

This document contains critical rules that MUST be followed in all code generation and commits.

## Rule 1: Class Name Generation
**NEVER** use dynamic class names (e.g., `bg-${color}` or template literals for Tailwind classes).

**ALWAYS** use full string class names (e.g., `bg-blue-500`, `text-gray-900`).

❌ **WRONG:**
```javascript
const colorClass = `bg-${color}-500`;
```

✅ **CORRECT:**
```javascript
const colorClasses = {
  blue: 'bg-blue-500',
  red: 'bg-red-500',
  green: 'bg-green-500'
};
const colorClass = colorClasses[color];
```

## Rule 2: Mobile-First Design
**ALWAYS** design mobile-first. Default styles should target mobile screens, with larger breakpoints applied via Tailwind's responsive prefixes.

**ALWAYS** use mobile-first breakpoints:
- Default: Mobile styles (no prefix)
- `sm:` - 640px and up
- `md:` - 768px and up
- `lg:` - 1024px and up
- `xl:` - 1280px and up
- `2xl:` - 1536px and up

**Examples:**
- ❌ **WRONG:** `flex-row md:flex-col` (desktop-first)
- ✅ **CORRECT:** `flex-col md:flex-row` (mobile-first)

- ❌ **WRONG:** `text-2xl md:text-base` (desktop-first)
- ✅ **CORRECT:** `text-base md:text-2xl` (mobile-first)

## Rule 3: Commit Protocol
**NEVER** automatically run `git add` or `git commit`.

**ALWAYS:**
1. Show `git diff --stat` summary before committing
2. Present the changes to the user
3. Wait for explicit user confirmation before executing commit commands
4. Only commit when user explicitly types "PROCEED TO COMMIT" or similar confirmation

This ensures the user maintains full control over version control operations.

---

**Last Updated:** Repository Initialization - Chapter 3
**Status:** Active

