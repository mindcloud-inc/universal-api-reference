# Google Dialogflow: Update Entity Type

Updates an existing entity type in Google Dialogflow.

```
PUT https://connect.mindcloud.co/v1/universal/googleDialogflow/latest/actions/update-entity-type
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Dialogflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/googleDialogflow/latest/actions/update-entity-type" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "projects/my-project/locations/global/agents/agent-id/entityTypes/entity-type-id",
  "body": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleDialogflow/latest/actions/update-entity-type', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "projects/my-project/locations/global/agents/agent-id/entityTypes/entity-type-id",
    "body": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `languageCode` | string | no | Optional BCP-47 language code for localized entity type fields. |
| `name` | string | yes | Required Dialogflow entity type resource name. Example: `projects/my-project/locations/global/agents/agent-id/entityTypes/entity-type-id`. |
| `body` | object | yes | Dialogflow EntityType fields to update. Example: `[object Object]`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `updateMask` | string | no | Optional field mask controlling which entity type fields are updated. Example: `displayName,entities`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "autoExpansionMode": "string",
      "displayName": "Ava Chen",
      "enableFuzzyExtraction": true,
      "entities": [
        {}
      ],
      "excludedPhrases": [
        {}
      ],
      "kind": "string",
      "name": "Ava Chen",
      "redact": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `autoExpansionMode` | string |  |
| `displayName` | string |  |
| `enableFuzzyExtraction` | boolean |  |
| `entities` | array<object> |  |
| `excludedPhrases` | array<object> |  |
| `kind` | string |  |
| `name` | string |  |
| `redact` | boolean |  |

## Native endpoint

Through the native Google Dialogflow API, this operation is `PATCH v3/:name` (base URL `https://dialogflow.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-entity-type.md) for the provider-specific parameters and requirements.

