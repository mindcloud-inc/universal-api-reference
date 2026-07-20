# Google Dialogflow: Create Entity Type

Creates a new entity type in Google Dialogflow.

```
POST https://connect.mindcloud.co/v1/universal/googleDialogflow/latest/actions/create-entity-type
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Dialogflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/googleDialogflow/latest/actions/create-entity-type" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "parent": "projects/my-project/locations/global/agents/agent-id",
  "body": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleDialogflow/latest/actions/create-entity-type', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "parent": "projects/my-project/locations/global/agents/agent-id",
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
| `parent` | string | yes | Required parent agent resource name for the new entity type. Example: `projects/my-project/locations/global/agents/agent-id`. |
| `body` | object | yes | Dialogflow EntityType request body. Example: `[object Object]`. |

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

Through the native Google Dialogflow API, this operation is `POST v3/:parent/entityTypes` (base URL `https://dialogflow.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-entity-type.md) for the provider-specific parameters and requirements.

