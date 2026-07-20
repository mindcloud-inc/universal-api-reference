# Google Dialogflow: Update Intent

Updates an existing intent in Google Dialogflow.

```
PUT https://connect.mindcloud.co/v1/universal/googleDialogflow/latest/actions/update-intent
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Dialogflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/googleDialogflow/latest/actions/update-intent" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "projects/my-project/locations/global/agents/agent-id/intents/intent-id",
  "body": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleDialogflow/latest/actions/update-intent', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "projects/my-project/locations/global/agents/agent-id/intents/intent-id",
    "body": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `languageCode` | string | no | Optional BCP-47 language code for localized intent fields. |
| `name` | string | yes | Required Dialogflow intent resource name. Example: `projects/my-project/locations/global/agents/agent-id/intents/intent-id`. |
| `body` | object | yes | Dialogflow Intent fields to update. Example: `[object Object]`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `updateMask` | string | no | Optional field mask controlling which intent fields are updated. Example: `displayName,priority`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "displayName": "Ava Chen",
      "isFallback": true,
      "labels": {},
      "name": "Ava Chen",
      "parameters": [
        {}
      ],
      "priority": 1,
      "trainingPhrases": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `displayName` | string |  |
| `isFallback` | boolean |  |
| `labels` | object |  |
| `name` | string |  |
| `parameters` | array<object> |  |
| `priority` | number |  |
| `trainingPhrases` | array<object> |  |

## Native endpoint

Through the native Google Dialogflow API, this operation is `PATCH v3/:name` (base URL `https://dialogflow.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-intent.md) for the provider-specific parameters and requirements.

