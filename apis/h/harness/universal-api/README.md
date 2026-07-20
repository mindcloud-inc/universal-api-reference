# <img src="https://images.mindcloud.co/apps/icons/83e3b54fdd2a62e0eb25cf68d96c579b_1773929660100.png" alt="Harness logo" width="28" height="28"> Harness: Universal API

Harness Platform integration for account, user, service account, and pipeline APIs using x-api-key authentication.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/harness/latest
- **Category:** IT Operations / DevOps
- **Actions:** 15
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://app.harness.io/
- **Vendor API docs:** https://apidocs.harness.io/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User Info](actions/get-current-user-info.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/harness/latest/actions/get-current-user-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (15)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account](actions/get-account.md) | GET | Retrieves an account from Harness. |

### Connector

| Action | Method | Description |
| --- | --- | --- |
| [Create Connector](actions/create-connector.md) | POST | Creates a new connector in Harness. |
| [Delete Connector](actions/delete-connector.md) | DELETE | Deletes a connector from Harness. |
| [List Connectors](actions/list-connectors.md) | GET | Retrieves connectors from Harness. |

### Input Set

| Action | Method | Description |
| --- | --- | --- |
| [Create Input Set](actions/create-input-set.md) | POST | Creates a new input set in Harness. |
| [Delete Input Set](actions/delete-input-set.md) | DELETE | Deletes an input set from Harness. |

### Pipeline

| Action | Method | Description |
| --- | --- | --- |
| [Create Pipeline](actions/create-pipeline.md) | POST | Creates a new pipeline in Harness. |
| [Delete Pipeline](actions/delete-pipeline.md) | DELETE | Deletes a pipeline from Harness. |
| [List Pipelines](actions/list-pipelines.md) | GET | Retrieves pipelines from Harness. |

### Pipeline Execution

| Action | Method | Description |
| --- | --- | --- |
| [Execute Pipeline With Input Set References](actions/execute-pipeline-with-input-set-references.md) | POST | Executes a Harness pipeline with input set references. |

### Service

| Action | Method | Description |
| --- | --- | --- |
| [List Services](actions/list-services.md) | GET | Retrieves services from Harness. |

### Service Account

| Action | Method | Description |
| --- | --- | --- |
| [List Service Accounts](actions/list-service-accounts.md) | GET | Retrieves service accounts from Harness. |

### Token

| Action | Method | Description |
| --- | --- | --- |
| [Validate Token](actions/validate-token.md) | GET | Validates an access token in Harness. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User Info](actions/get-current-user-info.md) | GET | Retrieves the current user from Harness. |
| [List Users](actions/list-users.md) | GET | Retrieves users from Harness. |

