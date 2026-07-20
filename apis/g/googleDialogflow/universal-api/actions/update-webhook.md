# Google Dialogflow: Update Webhook

Updates an existing webhook in Google Dialogflow.

```
PUT https://connect.mindcloud.co/v1/universal/googleDialogflow/latest/actions/update-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Dialogflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/googleDialogflow/latest/actions/update-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "projects/my-project/locations/global/agents/agent-id/webhooks/webhook-id",
  "body": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleDialogflow/latest/actions/update-webhook', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "projects/my-project/locations/global/agents/agent-id/webhooks/webhook-id",
    "body": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Required Dialogflow webhook resource name. Example: `projects/my-project/locations/global/agents/agent-id/webhooks/webhook-id`. |
| `body` | object | yes | Dialogflow Webhook fields to update. Example: `[object Object]`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `updateMask` | string | no | Optional field mask controlling which webhook fields are updated. Example: `displayName,timeout`. |

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

Through the native Google Dialogflow API, this operation is `PATCH v3/:name` (base URL `https://dialogflow.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-webhook.md) for the provider-specific parameters and requirements.

