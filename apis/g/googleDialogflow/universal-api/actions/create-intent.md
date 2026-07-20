# Google Dialogflow: Create Intent

Creates a new intent in Google Dialogflow.

```
POST https://connect.mindcloud.co/v1/universal/googleDialogflow/latest/actions/create-intent
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Dialogflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/googleDialogflow/latest/actions/create-intent" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "parent": "projects/my-project/locations/global/agents/agent-id",
  "body": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleDialogflow/latest/actions/create-intent', {
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
| `languageCode` | string | no | Optional BCP-47 language code for localized intent fields. |
| `parent` | string | yes | Required parent agent resource name for the new intent. Example: `projects/my-project/locations/global/agents/agent-id`. |
| `body` | object | yes | Dialogflow Intent request body. Example: `[object Object]`. |

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

Through the native Google Dialogflow API, this operation is `POST v3/:parent/intents` (base URL `https://dialogflow.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-intent.md) for the provider-specific parameters and requirements.

