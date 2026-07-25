```markdown
# stk_final Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches the core development patterns and conventions used in the `stk_final` TypeScript repository. It covers file naming, import/export styles, commit message practices, and testing patterns. While no specific frameworks or automated workflows are detected, this guide provides practical examples and suggested commands to streamline your development process.

## Coding Conventions

### File Naming
- **Convention:** Use camelCase for file names.
- **Example:**  
  ```plaintext
  userProfile.ts
  dataManager.ts
  ```

### Import Style
- **Convention:** Use relative imports for modules within the project.
- **Example:**
  ```typescript
  import { fetchData } from './apiClient';
  import { User } from '../models/user';
  ```

### Export Style
- **Convention:** Use named exports.
- **Example:**
  ```typescript
  // In userProfile.ts
  export function getUserProfile(id: string) { /* ... */ }
  export const DEFAULT_AVATAR = 'avatar.png';
  ```

### Commit Messages
- **Pattern:** Freeform messages, usually around 40 characters.
- **Example:**  
  ```
  Fix bug in user authentication flow
  Add support for new payment method
  ```

## Workflows

### Adding a New Module
**Trigger:** When you need to introduce a new feature or functionality.
**Command:** `/add-module`

1. Create a new file using camelCase (e.g., `featureName.ts`).
2. Use relative imports to include dependencies.
3. Export all functions or constants using named exports.
4. Write corresponding test files (see Testing Patterns).
5. Commit changes with a clear, concise message.

### Refactoring Existing Code
**Trigger:** When improving code readability or structure.
**Command:** `/refactor`

1. Identify the target file(s) and ensure file names follow camelCase.
2. Update import paths to remain relative.
3. Use named exports consistently.
4. Update or add tests if necessary.
5. Commit with a descriptive message.

### Writing Tests
**Trigger:** When adding or updating functionality.
**Command:** `/write-test`

1. Create a test file with the pattern `*.test.*` (e.g., `userProfile.test.ts`).
2. Write tests for each exported function or constant.
3. Use the project's preferred (unknown) testing framework.
4. Run tests to ensure correctness.
5. Commit test files with an appropriate message.

## Testing Patterns

- **File Pattern:** Test files should follow the `*.test.*` naming convention (e.g., `moduleName.test.ts`).
- **Framework:** The specific testing framework is not detected; follow project or team standards.
- **Example:**
  ```typescript
  // userProfile.test.ts
  import { getUserProfile } from './userProfile';

  describe('getUserProfile', () => {
    it('returns user data for a valid ID', () => {
      // test implementation
    });
  });
  ```

## Commands
| Command        | Purpose                                 |
|----------------|-----------------------------------------|
| /add-module    | Scaffold and add a new module           |
| /refactor      | Refactor existing code                  |
| /write-test    | Create and update test files            |
```
