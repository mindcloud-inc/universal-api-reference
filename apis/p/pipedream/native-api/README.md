# Pipedream: Native API Reference

A consolidated summary of Pipedream's API configuration and 28 documented operations, with links to official documentation.

- **Official docs:** https://pipedream.com/docs/rest-api/overview
- **API base URL:** `https://api.pipedream.com/v1`

## Authentication

### OAuth 2.0

Pipedream workspace OAuth client credentials.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Exchange the returned authorization code with a POST request to https://api.pipedream.com/v1/oauth/token.
2. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.


A machine-to-machine flow is configured.

[Official authentication documentation](https://pipedream.com/docs/rest-api/auth)

## Endpoints (28 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Automatically subscribe a listener to events from new workflows / sources](actions/auto-subscribe-listener-to-events.md) | `POST /auto_subscriptions` | [docs](https://pipedream.com/docs/rest-api/api-reference/subscription/automatically-subscribe-a-listener-to-events-from-new-workflows-sources) |
| [Create a component](actions/create-a-component.md) | `POST /components` | [docs](https://pipedream.com/docs/rest-api/api-reference/components/create-a-component) |
| [Create a source](actions/create-a-source.md) | `POST /sources` | [docs](https://pipedream.com/docs/rest-api/api-reference/sources/create-a-source) |
| [Create a webhook](actions/create-a-webhook.md) | `POST /webhooks` | [docs](https://pipedream.com/docs/rest-api/api-reference/webhooks/create-a-webhook) |
| [Create a workflow](actions/create-a-workflow.md) | `POST /workflows` | [docs](https://pipedream.com/docs/rest-api/api-reference/workflows/create-a-workflow) |
| [Delete a source](actions/delete-a-source.md) | `DELETE /sources/{id}` | [docs](https://pipedream.com/docs/rest-api/api-reference/sources/delete-a-source) |
| [Delete a subscription](actions/delete-a-subscription.md) | `DELETE /subscriptions` | [docs](https://pipedream.com/docs/rest-api/api-reference/subscription/delete-a-subscription) |
| [Delete a webhook](actions/delete-a-webhook.md) | `DELETE /webhooks/{id}` | [docs](https://pipedream.com/docs/rest-api/api-reference/webhooks/delete-a-webhook) |
| [Delete source events](actions/delete-source-events.md) | `DELETE /sources/{id}/events` | [docs](https://pipedream.com/docs/rest-api/api-reference/events/delete-source-events) |
| [Get a component](actions/get-a-component.md) | `GET /components/{key\|id}` | [docs](https://pipedream.com/docs/rest-api/api-reference/components/get-a-component) |
| [Get a component from the global registry](actions/get-a-component-from-the-global-registry.md) | `GET /components/registry/{key}` | [docs](https://pipedream.com/docs/rest-api/api-reference/components/get-a-component-from-the-global-registry) |
| [Get a new access token](actions/get-a-new-access-token.md) | `POST /oauth/token` | [docs](https://pipedream.com/docs/rest-api/api-reference/oauth/get-a-new-access-token) |
| [Get a workflow's details](actions/get-a-workflows-details.md) | `GET /workflows/{workflow_id}` | [docs](https://pipedream.com/docs/rest-api/api-reference/workflows/get-a-workflows-details) |
| [Get a workspace](actions/get-a-workspace.md) | `GET /workspaces/{org_id}` | [docs](https://pipedream.com/docs/rest-api/api-reference/workspaces/get-a-workspace) |
| [Get an app](actions/get-an-app.md) | `GET /apps/{app_id}` | [docs](https://pipedream.com/docs/rest-api/api-reference/apps/get-an-app) |
| [Get current user info](actions/get-current-user-info.md) | `GET /users/me` | [docs](https://pipedream.com/docs/rest-api/api-reference/users/get-current-user-info) |
| [Get source events](actions/get-source-events.md) | `GET /sources/{id}/event_summaries` | [docs](https://pipedream.com/docs/rest-api/api-reference/events/get-source-events) |
| [Get workflow emits](actions/get-workflows-emits.md) | `GET /workflows/{workflow_id}/event_summaries` | [docs](https://pipedream.com/docs/rest-api/api-reference/workflows/get-workflows-emits) |
| [Get workflow errors](actions/get-workflows-errors.md) | `GET /workflows/{workflow_id}/$errors/event_summaries` | [docs](https://pipedream.com/docs/rest-api/api-reference/workflows/get-workflows-errors) |
| [Get workspaces's sources](actions/get-workspaces-sources.md) | `GET /orgs/{org_id}/sources` | [docs](https://pipedream.com/docs/rest-api/api-reference/workspaces/get-workspaces-sources) |
| [Get workspaces's subscriptions](actions/get-workspaces-subscriptions.md) | `GET /workspaces/{org_id}/subscriptions` | [docs](https://pipedream.com/docs/rest-api/api-reference/workspaces/get-workspaces-subscriptions) |
| [Invoke workflow](actions/invoke-workflow.md) | `POST /workflows/{workflow_id}/invoke` | [docs](https://pipedream.com/docs/rest-api/api-reference/workflows/invoke-workflow) |
| [List apps](actions/list-apps.md) | `GET /apps` | [docs](https://pipedream.com/docs/rest-api/api-reference/apps/list-apps) |
| [Listen for events from another source or workflow](actions/listen-for-events-from-another-source-or-workflow.md) | `POST /subscriptions` | [docs](https://pipedream.com/docs/rest-api/api-reference/subscription/listen-for-events-from-another-source-or-workflow) |
| [Revoke an access token](actions/revoke-an-access-token.md) | `POST /oauth/revoke` | [docs](https://pipedream.com/docs/rest-api/api-reference/oauth/revoke-an-access-token) |
| [Search for registry components](actions/search-for-registry-components.md) | `GET /components/search` | [docs](https://pipedream.com/docs/rest-api/api-reference/components/search-for-registry-components) |
| [Update a source](actions/update-a-source.md) | `PUT /sources/{id}` | [docs](https://pipedream.com/docs/rest-api/api-reference/sources/update-a-source) |
| [Update a workflow](actions/update-a-workflow.md) | `PUT /workflows/{id}` | [docs](https://pipedream.com/docs/rest-api/api-reference/workflows/update-a-workflow) |
