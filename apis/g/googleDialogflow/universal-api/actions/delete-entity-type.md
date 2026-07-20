# Google Dialogflow: Delete Entity Type

Deletes an existing entity type from Google Dialogflow.

```
DELETE https://connect.mindcloud.co/v1/universal/googleDialogflow/latest/actions/delete-entity-type
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Dialogflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/googleDialogflow/latest/actions/delete-entity-type?connectionId=$CONNECTION_ID&name=projects%2Fmy-project%2Flocations%2Fglobal%2Fagents%2Fagent-id%2FentityTypes%2Fentity-type-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "name": "projects/my-project/locations/global/agents/agent-id/entityTypes/entity-type-id"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleDialogflow/latest/actions/delete-entity-type?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Required Dialogflow entity type resource name. Example: `projects/my-project/locations/global/agents/agent-id/entityTypes/entity-type-id`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `force` | boolean | no | Optional flag to force deletion when the provider supports it. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Google Dialogflow API returns.

## Native endpoint

Through the native Google Dialogflow API, this operation is `DELETE v3/:name` (base URL `https://dialogflow.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-entity-type.md) for the provider-specific parameters and requirements.

