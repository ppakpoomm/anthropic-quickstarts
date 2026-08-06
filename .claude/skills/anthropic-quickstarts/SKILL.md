```markdown
# anthropic-quickstarts Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches the core development patterns and conventions used in the `anthropic-quickstarts` Python repository. You'll learn about file naming, import/export styles, commit message habits, and how to structure and run tests. This guide is ideal for contributors seeking to align with the project's established practices.

## Coding Conventions

### File Naming
- Use **snake_case** for all file and module names.
  - Example: `example_module.py`

### Import Style
- Use **relative imports** within the package.
  - Example:
    ```python
    from .utils import helper_function
    ```

### Export Style
- Use **named exports**; explicitly define what is exported from modules.
  - Example:
    ```python
    def useful_function():
        pass

    __all__ = ['useful_function']
    ```

### Commit Patterns
- Commit messages are **freeform** (no strict prefixes), with an average length of ~49 characters.
  - Example:
    ```
    Add helper for API response formatting
    ```

## Workflows

### Adding a New Module
**Trigger:** When adding new functionality to the codebase  
**Command:** `/add-module`

1. Create a new Python file using snake_case naming (e.g., `new_feature.py`).
2. Implement your functionality.
3. Use relative imports for internal dependencies.
4. Define `__all__` to specify exported objects.
5. Write or update tests as appropriate.

### Updating an Existing Module
**Trigger:** When modifying or extending existing features  
**Command:** `/update-module`

1. Locate the target module (e.g., `existing_feature.py`).
2. Make your changes, maintaining snake_case and relative imports.
3. Update `__all__` if new exports are added.
4. Update or add tests to cover changes.

### Writing a Commit
**Trigger:** When committing changes  
**Command:** `/write-commit`

1. Write a concise, descriptive commit message (~49 chars).
2. No strict prefix required.
3. Example:
    ```
    Refactor input validation logic in utils
    ```

## Testing Patterns

- **Framework:** Unknown (not detected), but test files follow the `*.test.ts` pattern (TypeScript).
- **Location:** Test files are named with `.test.ts` suffix.
- **Note:** Since the main codebase is Python and tests are in TypeScript, ensure to keep language boundaries clear and coordinate test coverage accordingly.

## Commands
| Command         | Purpose                                            |
|-----------------|---------------------------------------------------|
| /add-module     | Scaffold and add a new Python module              |
| /update-module  | Update or extend an existing module               |
| /write-commit   | Write a commit message following project style    |

```