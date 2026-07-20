# Google Dialogflow: Native API Reference

A consolidated summary of Google Dialogflow's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://docs.cloud.google.com/dialogflow/docs
- **OpenAPI specification:** https://dialogflow.googleapis.com/$discovery/rest?version=v3
- **API base URL:** `https://dialogflow.googleapis.com`

## Authentication

### Google OAuth 2.0

Connect with a Google account that has access to Dialogflow CX resources.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://accounts.google.com/o/oauth2/v2/auth to approve access.
2. Exchange the returned authorization code with a POST request to https://oauth2.googleapis.com/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `https://www.googleapis.com/auth/dialogflow`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://oauth2.googleapis.com/token.

[Official authentication documentation](https://developers.google.com/identity/protocols/oauth2/web-server)

### Service Account

Authenticate Google Dialogflow with a Google Cloud service account private key.

### Credentials

- **Project ID:** `project` · required · The Google Cloud project ID that contains the Dialogflow resources this connection should access.
- **Client Email:** `clientEmail` · required · The client_email value from the service account key JSON file.
- **Private Key ID:** `privateKeyId` · optional · Optional legacy field from the service account key JSON file. The Google auth SDK can mint Dialogflow access tokens with only project ID, client email, and private key.
- **Private Key:** `privateKeySecret` · required · The private_key value from the service account key JSON file. MindCloud uses it only to sign short-lived Google OAuth JWT assertions.

[Official authentication documentation](https://developers.google.com/identity/protocols/oauth2/service-account)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `pageSize` in the query string to set the page size (default 100; accepted range 1–1000). Use `pageToken` in the query string as the pagination cursor; numbering starts at 0.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Agent](actions/create-agent.md) | `POST v3/:parent/agents` | [docs](https://docs.cloud.google.com/dialogflow/cx/docs/reference/rest/v3/projects.locations.agents/create) |
| [Create Entity Type](actions/create-entity-type.md) | `POST v3/:parent/entityTypes` | [docs](https://docs.cloud.google.com/dialogflow/cx/docs/reference/rest/v3/projects.locations.agents.entityTypes/create) |
| [Create Flow](actions/create-flow.md) | `POST v3/:parent/flows` | [docs](https://docs.cloud.google.com/dialogflow/cx/docs/reference/rest/v3/projects.locations.agents.flows/create) |
| [Create Intent](actions/create-intent.md) | `POST v3/:parent/intents` | [docs](https://docs.cloud.google.com/dialogflow/cx/docs/reference/rest/v3/projects.locations.agents.intents/create) |
| [Create Page](actions/create-page.md) | `POST v3/:parent/pages` | [docs](https://docs.cloud.google.com/dialogflow/cx/docs/reference/rest/v3/projects.locations.agents.flows.pages/create) |
| [Create Webhook](actions/create-webhook.md) | `POST v3/:parent/webhooks` | [docs](https://docs.cloud.google.com/dialogflow/cx/docs/reference/rest/v3/projects.locations.agents.webhooks/create) |
| [Delete Agent](actions/delete-agent.md) | `DELETE v3/:name` | [docs](https://docs.cloud.google.com/dialogflow/cx/docs/reference/rest/v3/projects.locations.agents/delete) |
| [Delete Entity Type](actions/delete-entity-type.md) | `DELETE v3/:name` | [docs](https://docs.cloud.google.com/dialogflow/cx/docs/reference/rest/v3/projects.locations.agents.entityTypes/delete) |
| [Delete Flow](actions/delete-flow.md) | `DELETE v3/:name` | [docs](https://docs.cloud.google.com/dialogflow/cx/docs/reference/rest/v3/projects.locations.agents.flows/delete) |
| [Delete Intent](actions/delete-intent.md) | `DELETE v3/:name` | [docs](https://docs.cloud.google.com/dialogflow/cx/docs/reference/rest/v3/projects.locations.agents.intents/delete) |
| [Delete Page](actions/delete-page.md) | `DELETE v3/:name` | [docs](https://docs.cloud.google.com/dialogflow/cx/docs/reference/rest/v3/projects.locations.agents.flows.pages/delete) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE v3/:name` | [docs](https://docs.cloud.google.com/dialogflow/cx/docs/reference/rest/v3/projects.locations.agents.webhooks/delete) |
| [Export Agent](actions/export-agent.md) | `POST v3/:name:export` | [docs](https://docs.cloud.google.com/dialogflow/cx/docs/reference/rest/v3/projects.locations.agents/export) |
| [Export Flow](actions/export-flow.md) | `POST v3/:name:export` | [docs](https://docs.cloud.google.com/dialogflow/cx/docs/reference/rest/v3/projects.locations.agents.flows/export) |
| [Get Agent](actions/get-agent.md) | `GET v3/:name` | [docs](https://docs.cloud.google.com/dialogflow/cx/docs/reference/rest/v3/projects.locations.agents/get) |
| [Get Agent Validation Result](actions/get-agent-validation-result.md) | `GET v3/:name` | [docs](https://docs.cloud.google.com/dialogflow/cx/docs/reference/rest/v3/projects.locations.agents/getValidationResult) |
| [Get Entity Type](actions/get-entity-type.md) | `GET v3/:name` | [docs](https://docs.cloud.google.com/dialogflow/cx/docs/reference/rest/v3/projects.locations.agents.entityTypes/get) |
| [Get Flow](actions/get-flow.md) | `GET v3/:name` | [docs](https://docs.cloud.google.com/dialogflow/cx/docs/reference/rest/v3/projects.locations.agents.flows/get) |
| [Get Flow Validation Result](actions/get-flow-validation-result.md) | `GET v3/:name` | [docs](https://docs.cloud.google.com/dialogflow/cx/docs/reference/rest/v3/projects.locations.agents.flows/getValidationResult) |
| [Get Intent](actions/get-intent.md) | `GET v3/:name` | [docs](https://docs.cloud.google.com/dialogflow/cx/docs/reference/rest/v3/projects.locations.agents.intents/get) |
| [Get Location](actions/get-location.md) | `GET v3/:name` | [docs](https://docs.cloud.google.com/dialogflow/cx/docs/reference/rest/v3/projects.locations/get) |
| [Get Page](actions/get-page.md) | `GET v3/:name` | [docs](https://docs.cloud.google.com/dialogflow/cx/docs/reference/rest/v3/projects.locations.agents.flows.pages/get) |
| [Get Webhook](actions/get-webhook.md) | `GET v3/:name` | [docs](https://docs.cloud.google.com/dialogflow/cx/docs/reference/rest/v3/projects.locations.agents.webhooks/get) |
| [Import Flow](actions/import-flow.md) | `POST v3/:parent/flows:import` | [docs](https://docs.cloud.google.com/dialogflow/cx/docs/reference/rest/v3/projects.locations.agents.flows/import) |
| [List Agents](actions/list-agents.md) | `GET v3/:parent/agents` | [docs](https://docs.cloud.google.com/dialogflow/cx/docs/reference/rest/v3/projects.locations.agents/list) |
| [List Entity Types](actions/list-entity-types.md) | `GET v3/:parent/entityTypes` | [docs](https://docs.cloud.google.com/dialogflow/cx/docs/reference/rest/v3/projects.locations.agents.entityTypes/list) |
| [List Flows](actions/list-flows.md) | `GET v3/:parent/flows` | [docs](https://docs.cloud.google.com/dialogflow/cx/docs/reference/rest/v3/projects.locations.agents.flows/list) |
| [List Intents](actions/list-intents.md) | `GET v3/:parent/intents` | [docs](https://docs.cloud.google.com/dialogflow/cx/docs/reference/rest/v3/projects.locations.agents.intents/list) |
| [List Locations](actions/list-locations.md) | `GET v3/:name/locations` | [docs](https://docs.cloud.google.com/dialogflow/cx/docs/reference/rest/v3/projects.locations/list) |
| [List Pages](actions/list-pages.md) | `GET v3/:parent/pages` | [docs](https://docs.cloud.google.com/dialogflow/cx/docs/reference/rest/v3/projects.locations.agents.flows.pages/list) |
| [List Webhooks](actions/list-webhooks.md) | `GET v3/:parent/webhooks` | [docs](https://docs.cloud.google.com/dialogflow/cx/docs/reference/rest/v3/projects.locations.agents.webhooks/list) |
| [Train Flow](actions/train-flow.md) | `POST v3/:name:train` | [docs](https://docs.cloud.google.com/dialogflow/cx/docs/reference/rest/v3/projects.locations.agents.flows/train) |
| [Update Agent](actions/update-agent.md) | `PATCH v3/:name` | [docs](https://docs.cloud.google.com/dialogflow/cx/docs/reference/rest/v3/projects.locations.agents/patch) |
| [Update Entity Type](actions/update-entity-type.md) | `PATCH v3/:name` | [docs](https://docs.cloud.google.com/dialogflow/cx/docs/reference/rest/v3/projects.locations.agents.entityTypes/patch) |
| [Update Flow](actions/update-flow.md) | `PATCH v3/:name` | [docs](https://docs.cloud.google.com/dialogflow/cx/docs/reference/rest/v3/projects.locations.agents.flows/patch) |
| [Update Intent](actions/update-intent.md) | `PATCH v3/:name` | [docs](https://docs.cloud.google.com/dialogflow/cx/docs/reference/rest/v3/projects.locations.agents.intents/patch) |
| [Update Page](actions/update-page.md) | `PATCH v3/:name` | [docs](https://docs.cloud.google.com/dialogflow/cx/docs/reference/rest/v3/projects.locations.agents.flows.pages/patch) |
| [Update Webhook](actions/update-webhook.md) | `PATCH v3/:name` | [docs](https://docs.cloud.google.com/dialogflow/cx/docs/reference/rest/v3/projects.locations.agents.webhooks/patch) |
| [Validate Agent](actions/validate-agent.md) | `POST v3/:name:validate` | [docs](https://docs.cloud.google.com/dialogflow/cx/docs/reference/rest/v3/projects.locations.agents/validate) |
| [Validate Flow](actions/validate-flow.md) | `POST v3/:name:validate` | [docs](https://docs.cloud.google.com/dialogflow/cx/docs/reference/rest/v3/projects.locations.agents.flows/validate) |
