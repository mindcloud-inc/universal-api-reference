# Synthflow AI Phone Calling: Native API Reference

A consolidated summary of Synthflow AI Phone Calling's API configuration and 34 documented operations, with links to official documentation.

- **Official docs:** https://docs.synthflow.ai/reference/getting-started-with-your-api
- **API base URL:** `https://api.synthflow.ai/v2`

## Authentication

### API Key

Authenticate with a Synthflow API key using Bearer token authentication.

### Credentials

- **API Key:** `apiKey` · required
- **Workspace ID:** `workspaceId` · required · The Synthflow workspace ID required by workspace-scoped endpoints.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.synthflow.ai/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (34 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Agent](actions/create-agent.md) | `POST /assistants` | [docs](https://docs.synthflow.ai/api-reference/platform-api/agents/create-assistant) |
| [Create Contact](actions/create-contact.md) | `POST /contacts` | [docs](https://docs.synthflow.ai/api-reference/platform-api/contacts) |
| [Create Phone Book](actions/create-phone-book.md) | `POST /phonebooks` | [docs](https://docs.synthflow.ai/api-reference/platform-api/phone-books/create-a-phone-book) |
| [Create Phone Book Entry](actions/create-phone-book-entry.md) | `POST /phonebooks/:phone_book_id/entries` | [docs](https://docs.synthflow.ai/api-reference/platform-api/phone-books/create-a-phone-book-entry) |
| [Create Simulation Case](actions/create-simulation-case.md) | `POST /simulation_cases` | [docs](https://docs.synthflow.ai/api-reference/platform-api/simulations/create-simulation-case) |
| [Delete Agent](actions/delete-agent.md) | `DELETE /assistants/:model_id` | [docs](https://docs.synthflow.ai/api-reference/platform-api/agents/delete-assistant) |
| [Delete Contact](actions/delete-contact.md) | `DELETE /contacts/:contact_id` | [docs](https://docs.synthflow.ai/api-reference/platform-api/contacts/delete-a-contact) |
| [Delete Phone Book](actions/delete-phone-book.md) | `DELETE /phonebooks/:phone_book_id` | [docs](https://docs.synthflow.ai/api-reference/platform-api/phone-books/delete-a-phone-book) |
| [Delete Phone Book Entry](actions/delete-phone-book-entry.md) | `DELETE /phonebooks/:phone_book_id/entries/:entry_id` | [docs](https://docs.synthflow.ai/api-reference/platform-api/phone-books/delete-a-phone-book-entry) |
| [Delete Simulation Case](actions/delete-simulation-case.md) | `DELETE /simulation_cases/:simulation_case_id` | [docs](https://docs.synthflow.ai/api-reference/platform-api/simulations/delete-simulation-case) |
| [Generate Test Cases](actions/generate-test-cases.md) | `POST /simulation_cases/generate` | [docs](https://docs.synthflow.ai/api-reference/platform-api/simulations/generate-test-cases) |
| [Get Agent](actions/get-agent.md) | `GET /assistants/:model_id` | [docs](https://docs.synthflow.ai/api-reference/platform-api/agents/get-assistant) |
| [Get Call](actions/get-call.md) | `GET /calls/:call_id` | [docs](https://docs.synthflow.ai/api-reference/platform-api/calls/get-phone-call) |
| [Get Contact](actions/get-contact.md) | `GET /contacts/:contact_id` | [docs](https://docs.synthflow.ai/api-reference/platform-api/contacts/get-a-contact) |
| [Get Phone Number](actions/get-phone-number.md) | `GET /numbers/:phone_number_slug` | [docs](https://docs.synthflow.ai/api-reference/platform-api/phone-numbers/get-phone-number) |
| [Get Simulation](actions/get-simulation.md) | `GET /simulations/:simulation_id` | [docs](https://docs.synthflow.ai/api-reference/platform-api/simulations/get-simulation) |
| [Get Simulation Case](actions/get-simulation-case.md) | `GET /simulation_cases/:simulation_case_id` | [docs](https://docs.synthflow.ai/api-reference/platform-api/simulations/get-simulation-case) |
| [Get Simulation Session](actions/get-simulation-session.md) | `GET /simulation_sessions/:simulation_session_id` | [docs](https://docs.synthflow.ai/api-reference/platform-api/simulations/get-simulation-session) |
| [Get Webhook Log](actions/get-webhook-log.md) | `GET /logs/:webhook_log_id` | [docs](https://docs.synthflow.ai/api-reference/platform-api/webhook-logs/get-webhook-log-detail) |
| [List Actions](actions/list-actions.md) | `GET /actions` | [docs](https://docs.synthflow.ai/api-reference/platform-api/actions/list-actions) |
| [List Agents](actions/list-agents.md) | `GET /assistants` | [docs](https://docs.synthflow.ai/api-reference/platform-api/agents/list-assistant) |
| [List Calls](actions/list-calls.md) | `GET /calls` | [docs](https://docs.synthflow.ai/api-reference/platform-api/calls/list-calls) |
| [List Contacts](actions/list-contacts.md) | `GET /contacts` | [docs](https://docs.synthflow.ai/api-reference/platform-api/contacts/list-contacts) |
| [List Phone Books](actions/list-phone-books.md) | `GET /phonebooks` | [docs](https://docs.synthflow.ai/api-reference/platform-api/phone-books/list-phone-books) |
| [List Phone Numbers](actions/list-phone-numbers.md) | `GET /numbers` | [docs](https://docs.synthflow.ai/api-reference/platform-api/phone-numbers/get-numbers) |
| [List Simulation Cases](actions/list-simulation-cases.md) | `GET /simulation_cases` | [docs](https://docs.synthflow.ai/api-reference/platform-api/simulations/list-simulation-cases) |
| [List Simulation Cases By Agent](actions/list-simulation-cases-by-agent.md) | `GET /simulation_cases/by_agent` | [docs](https://docs.synthflow.ai/api-reference/platform-api/simulations/list-simulation-cases-by-agent) |
| [List Simulation Sessions](actions/list-simulation-sessions.md) | `GET /simulation_sessions` | [docs](https://docs.synthflow.ai/api-reference/platform-api/simulations/list-simulation-sessions) |
| [List Simulations](actions/list-simulations.md) | `GET /simulations` | [docs](https://docs.synthflow.ai/api-reference/platform-api/simulations/list-simulations) |
| [List Webhook Logs](actions/list-webhook-logs.md) | `GET /logs` | [docs](https://docs.synthflow.ai/api-reference/platform-api/webhook-logs/list-webhook-logs) |
| [Start Simulation](actions/start-simulation.md) | `POST /simulations/start` | [docs](https://docs.synthflow.ai/api-reference/platform-api/simulations/start-simulation) |
| [Update Agent](actions/update-agent.md) | `PUT /assistants/:model_id` | [docs](https://docs.synthflow.ai/api-reference/platform-api/agents/update-assistant) |
| [Update Contact](actions/update-contact.md) | `PATCH /contacts/:contact_id` | [docs](https://docs.synthflow.ai/api-reference/platform-api/contacts/update-a-contact) |
| [Update Simulation Case](actions/update-simulation-case.md) | `PUT /simulation_cases/:simulation_case_id` | [docs](https://docs.synthflow.ai/api-reference/platform-api/simulations/update-simulation-case) |
