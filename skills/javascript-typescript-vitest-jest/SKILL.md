---
name: javascript-typescript-vitest-jest
description: 'Best practices for writing JavaScript/TypeScript tests using Vitest and Jest, including mocking strategies, test structure, and common patterns.'
---

### Test Structure
- Name test files with `.test.ts` or `.test.js` suffix
- Place test files next to the code they test or in a dedicated `__tests__` directory
- Use descriptive test names that explain the expected behavior
- Use nested describe blocks to organize related tests
- Follow the pattern: `describe('Component/Function/Class', () => { it('should do something', () => {}) })`

### Effective Mocking
- Mock external dependencies (APIs, databases, etc.) to isolate your tests
- Use `vi.mock()` in Vitest or `jest.mock()` in Jest for module-level mocks
- Use `vi.spyOn()` in Vitest or `jest.spyOn()` in Jest for specific function mocks
- Use `mockImplementation()` or `mockReturnValue()` to define mock behavior
- Reset mocks between tests with `vi.resetAllMocks()` or `jest.resetAllMocks()` in `afterEach`
- Restore spies when needed with `vi.restoreAllMocks()` or `jest.restoreAllMocks()`

### Testing Async Code
- Always return promises or use async/await syntax in tests
- Use `resolves`/`rejects` matchers for promises
- Set appropriate timeouts for slow tests with `vi.setTimeout()` in Vitest or `jest.setTimeout()` in Jest

### Snapshot Testing
- Use snapshot tests for UI components or complex objects that change infrequently
- Keep snapshots small and focused
- Review snapshot changes carefully before committing

### Testing React Components
- Use React Testing Library over Enzyme for testing components
- Test user behavior and component accessibility
- Query elements by accessibility roles, labels, or text content
- Use `userEvent` over `fireEvent` for more realistic user interactions

## Common Vitest and Jest Matchers
- Basic: `expect(value).toBe(expected)`, `expect(value).toEqual(expected)`
- Truthiness: `expect(value).toBeTruthy()`, `expect(value).toBeFalsy()`
- Numbers: `expect(value).toBeGreaterThan(3)`, `expect(value).toBeLessThanOrEqual(3)`
- Strings: `expect(value).toMatch(/pattern/)`, `expect(value).toContain('substring')`
- Arrays: `expect(array).toContain(item)`, `expect(array).toHaveLength(3)`
- Objects: `expect(object).toHaveProperty('key', value)`
- Exceptions: `expect(fn).toThrow()`, `expect(fn).toThrow(Error)`
- Mock functions: `expect(mockFn).toHaveBeenCalled()`, `expect(mockFn).toHaveBeenCalledWith(arg1, arg2)`

## Vitest and Jest Notes
- Use `vi` in Vitest and `jest` in Jest for test utilities, timers, and module mocking
- Prefer `describe`, `it`, `test`, `beforeEach`, `afterEach`, `beforeAll`, and `afterAll` from the active runner
- Keep assertions runner-agnostic unless a runner-specific helper is required