# Google Dialogflow: Create Webhook

Creates a new webhook in Google Dialogflow.

```
POST https://connect.mindcloud.co/v1/universal/googleDialogflow/latest/actions/create-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Dialogflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/googleDialogflow/latest/actions/create-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "parent": "projects/my-project/locations/global/agents/agent-id",
  "body": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleDialogflow/latest/actions/create-webhook', {
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
| `parent` | string | yes | Required parent agent resource name for the new webhook. Example: `projects/my-project/locations/global/agents/agent-id`. |
| `body` | object | yes | Dialogflow Webhook request body. Example: `[object Object]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "disabled": true,
      "displayName": "Ava Chen",
      "genericWebService": {},
      "name": "Ava Chen",
      "serviceDirectory": {},
      "timeout": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `disabled` | boolean |  |
| `displayName` | string |  |
| `genericWebService` | object |  |
| `name` | string |  |
| `serviceDirectory` | object |  |
| `timeout` | string |  |

## Native endpoint

Through the native Google Dialogflow API, this operation is `POST v3/:parent/webhooks` (base URL `https://dialogflow.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webhook.md) for the provider-specific parameters and requirements.

