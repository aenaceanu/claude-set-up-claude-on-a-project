# CLAUDE.md

## Project context
This is a small Express API starter with an in-memory data store. The app is designed to be easy to reason about and easy to test.

## Important implementation details
- The server entry point is `server.js`; it mounts the `/users` and `/health` route modules.
- `routes/users.js` handles user listing, fetching by id, and creation.
- `db/store.js` is intentionally in-memory only; it resets whenever the process restarts.
- Validation is done in the route layer, not in the data store.

## Commands
- `npm test` — run the Node test suite.
- `npm run lint` — eslint validation.
- `npm run dev` — development mode with file watching.
- `npm start` — production-style launch.

## Guidance for changes
- Keep the API behavior consistent with the existing patterns: `400` for invalid input, `404` for missing records, `201` for created users.
- Use the real app and `supertest` for tests, rather than mocking route logic.
- Prefer minimal code changes and preserve the project's simple architecture.
- Do not add persistence or database features unless the task explicitly asks for them.
- Before finishing a task, run the relevant validation commands and make sure the tests still pass.
