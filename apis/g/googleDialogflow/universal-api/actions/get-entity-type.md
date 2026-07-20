# Google Dialogflow: Get Entity Type

Retrieves an entity type from Google Dialogflow.

```
GET https://connect.mindcloud.co/v1/universal/googleDialogflow/latest/actions/get-entity-type
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Dialogflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleDialogflow/latest/actions/get-entity-type?connectionId=$CONNECTION_ID&name=projects%2Fmy-project%2Flocations%2Fglobal%2Fagents%2Fagent-id%2FentityTypes%2Fentity-type-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "name": "projects/my-project/locations/global/agents/agent-id/entityTypes/entity-type-id"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleDialogflow/latest/actions/get-entity-type?${params}`, {
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
| `languageCode` | string | no | Optional BCP-47 language code for localized entity type fields. |
| `name` | string | no | Required Dialogflow entity type resource name. |
| `name` | string | yes | Required Dialogflow entity type resource name. Example: `projects/my-project/locations/global/agents/agent-id/entityTypes/entity-type-id`. |

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

Through the native Google Dialogflow API, this operation is `GET v3/:name` (base URL `https://dialogflow.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-entity-type.md) for the provider-specific parameters and requirements.

