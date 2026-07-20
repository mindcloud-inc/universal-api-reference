# <img src="https://images.mindcloud.co/apps/icons/google-dialogflow_1776347916477.png" alt="Google Dialogflow logo" width="28" height="28"> Google Dialogflow: Universal API

Build and manage Google Dialogflow CX conversational agents, flows, intents, entity types, pages, and webhooks through the Dialogflow API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/googleDialogflow/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://cloud.google.com/dialogflow
- **Vendor API docs:** https://docs.cloud.google.com/dialogflow/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Locations](actions/list-locations.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleDialogflow/latest/actions/list-locations?connectionId=$CONNECTION_ID&limit=25&offset=0&name=projects%2Fmy-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Agent

| Action | Method | Description |
| --- | --- | --- |
| [Create Agent](actions/create-agent.md) | POST | Creates a new agent in Google Dialogflow. |
| [Delete Agent](actions/delete-agent.md) | DELETE | Deletes an existing agent from Google Dialogflow. |
| [Export Agent](actions/export-agent.md) | GET | Exports an agent from Google Dialogflow. |
| [Get Agent](actions/get-agent.md) | GET | Retrieves an agent from Google Dialogflow. |
| [List Agents](actions/list-agents.md) | GET | Retrieves agents from Google Dialogflow. |
| [Update Agent](actions/update-agent.md) | PUT | Updates an existing agent in Google Dialogflow. |
| [Validate Agent](actions/validate-agent.md) | GET | Validates an agent in Google Dialogflow. |

### Agent Validation Result

| Action | Method | Description |
| --- | --- | --- |
| [Get Agent Validation Result](actions/get-agent-validation-result.md) | GET | Retrieves an agent validation result from Google Dialogflow. |

### Entity Type

| Action | Method | Description |
| --- | --- | --- |
| [Create Entity Type](actions/create-entity-type.md) | POST | Creates a new entity type in Google Dialogflow. |
| [Delete Entity Type](actions/delete-entity-type.md) | DELETE | Deletes an existing entity type from Google Dialogflow. |
| [Get Entity Type](actions/get-entity-type.md) | GET | Retrieves an entity type from Google Dialogflow. |
| [List Entity Types](actions/list-entity-types.md) | GET | Retrieves entity types from Google Dialogflow. |
| [Update Entity Type](actions/update-entity-type.md) | PUT | Updates an existing entity type in Google Dialogflow. |

### Flow

| Action | Method | Description |
| --- | --- | --- |
| [Create Flow](actions/create-flow.md) | POST | Creates a new flow in Google Dialogflow. |
| [Delete Flow](actions/delete-flow.md) | DELETE | Deletes an existing flow from Google Dialogflow. |
| [Export Flow](actions/export-flow.md) | GET | Exports a flow from Google Dialogflow. |
| [Get Flow](actions/get-flow.md) | GET | Retrieves a flow from Google Dialogflow. |
| [Import Flow](actions/import-flow.md) | POST | Imports a flow into Google Dialogflow. |
| [List Flows](actions/list-flows.md) | GET | Retrieves flows from Google Dialogflow. |
| [Train Flow](actions/train-flow.md) | PUT | Trains a flow in Google Dialogflow. |
| [Update Flow](actions/update-flow.md) | PUT | Updates an existing flow in Google Dialogflow. |
| [Validate Flow](actions/validate-flow.md) | GET | Validates a flow in Google Dialogflow. |

### Flow Validation Result

| Action | Method | Description |
| --- | --- | --- |
| [Get Flow Validation Result](actions/get-flow-validation-result.md) | GET | Retrieves a flow validation result from Google Dialogflow. |

### Intent

| Action | Method | Description |
| --- | --- | --- |
| [Create Intent](actions/create-intent.md) | POST | Creates a new intent in Google Dialogflow. |
| [Delete Intent](actions/delete-intent.md) | DELETE | Deletes an existing intent from Google Dialogflow. |
| [Get Intent](actions/get-intent.md) | GET | Retrieves an intent from Google Dialogflow. |
| [List Intents](actions/list-intents.md) | GET | Retrieves intents from Google Dialogflow. |
| [Update Intent](actions/update-intent.md) | PUT | Updates an existing intent in Google Dialogflow. |

### Location

| Action | Method | Description |
| --- | --- | --- |
| [Get Location](actions/get-location.md) | GET | Retrieves a location from Google Dialogflow. |
| [List Locations](actions/list-locations.md) | GET | Retrieves locations from Google Dialogflow. |

### Page

| Action | Method | Description |
| --- | --- | --- |
| [Create Page](actions/create-page.md) | POST | Creates a new page in Google Dialogflow. |
| [Delete Page](actions/delete-page.md) | DELETE | Deletes an existing page from Google Dialogflow. |
| [Get Page](actions/get-page.md) | GET | Retrieves a page from Google Dialogflow. |
| [List Pages](actions/list-pages.md) | GET | Retrieves pages from Google Dialogflow. |
| [Update Page](actions/update-page.md) | PUT | Updates an existing page in Google Dialogflow. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a new webhook in Google Dialogflow. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes an existing webhook from Google Dialogflow. |
| [Get Webhook](actions/get-webhook.md) | GET | Retrieves a webhook from Google Dialogflow. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves webhooks from Google Dialogflow. |
| [Update Webhook](actions/update-webhook.md) | PUT | Updates an existing webhook in Google Dialogflow. |

