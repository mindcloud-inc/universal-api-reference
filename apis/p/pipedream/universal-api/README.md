# <img src="https://images.mindcloud.co/apps/icons/pipedream_1776265444480.png" alt="Pipedream logo" width="28" height="28"> Pipedream: Universal API

Connect to Pipedream's REST API for workflows, apps, sources, and account data.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/pipedream/latest
- **Category:** IT Operations / Integration & Automation
- **Actions:** 28
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://pipedream.com
- **Vendor API docs:** https://pipedream.com/docs/rest-api/overview

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List apps](actions/list-apps.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pipedream/latest/actions/list-apps?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (28)

### Access Tokens

| Action | Method | Description |
| --- | --- | --- |
| [Get a new access token](actions/get-a-new-access-token.md) | POST | Creates a new OAuth access token in Pipedream. |
| [Revoke an access token](actions/revoke-an-access-token.md) | DELETE | Revokes an OAuth access token in Pipedream. |

### Applications

| Action | Method | Description |
| --- | --- | --- |
| [Get an app](actions/get-an-app.md) | GET | Retrieves details for an app from Pipedream. |
| [List apps](actions/list-apps.md) | GET | Retrieves a list of apps from Pipedream. |

### Data Sources

| Action | Method | Description |
| --- | --- | --- |
| [Create a source](actions/create-a-source.md) | POST | Creates a new source in Pipedream. |
| [Delete a source](actions/delete-a-source.md) | DELETE | Deletes an existing source from Pipedream. |
| [Get workspaces's sources](actions/get-workspaces-sources.md) | GET | Retrieves sources for a workspace from Pipedream. |
| [Update a source](actions/update-a-source.md) | PUT | Updates an existing source in Pipedream. |

### Events

| Action | Method | Description |
| --- | --- | --- |
| [Delete source events](actions/delete-source-events.md) | DELETE | Deletes all events for a source in Pipedream. |
| [Get source events](actions/get-source-events.md) | GET | Retrieves event summaries for a source in Pipedream. |
| [Get workflow emits](actions/get-workflows-emits.md) | GET | Retrieves emitted event summaries for a workflow in Pipedream. |
| [Get workflow errors](actions/get-workflows-errors.md) | GET | Retrieves error event summaries for a workflow in Pipedream. |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Create a component](actions/create-a-component.md) | POST | Creates a new component in Pipedream. |
| [Get a component](actions/get-a-component.md) | GET | Retrieves a component from Pipedream by ID or key. |
| [Get a component from the global registry](actions/get-a-component-from-the-global-registry.md) | GET | Retrieves a registry component from Pipedream by key. |
| [Search for registry components](actions/search-for-registry-components.md) | GET | Finds registry components in Pipedream by natural-language query. |

### Subscriptions

| Action | Method | Description |
| --- | --- | --- |
| [Automatically subscribe a listener to events from new workflows / sources](actions/auto-subscribe-listener-to-events.md) | POST | Creates an auto-subscription for new workflow or source events in Pipedream. |
| [Delete a subscription](actions/delete-a-subscription.md) | DELETE | Deletes an existing subscription from Pipedream. |
| [Get workspaces's subscriptions](actions/get-workspaces-subscriptions.md) | GET | Retrieves subscriptions for a workspace from Pipedream. |
| [Listen for events from another source or workflow](actions/listen-for-events-from-another-source-or-workflow.md) | POST | Creates a subscription to source or workflow events in Pipedream. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get current user info](actions/get-current-user-info.md) | GET | Retrieves the current user's details from Pipedream. |

### Webhook Endpoints

| Action | Method | Description |
| --- | --- | --- |
| [Create a webhook](actions/create-a-webhook.md) | POST | Creates a new webhook in Pipedream. |
| [Delete a webhook](actions/delete-a-webhook.md) | DELETE | Deletes an existing webhook from Pipedream. |

### Workflows

| Action | Method | Description |
| --- | --- | --- |
| [Create a workflow](actions/create-a-workflow.md) | POST | Creates a new workflow in Pipedream. |
| [Get a workflow's details](actions/get-a-workflows-details.md) | GET | Retrieves details for a workflow from Pipedream. |
| [Invoke workflow](actions/invoke-workflow.md) | POST | Invokes a workflow run in Pipedream. |
| [Update a workflow](actions/update-a-workflow.md) | PUT | Updates an existing workflow in Pipedream. |

### Workspaces

| Action | Method | Description |
| --- | --- | --- |
| [Get a workspace](actions/get-a-workspace.md) | GET | Retrieves details for a workspace from Pipedream. |

