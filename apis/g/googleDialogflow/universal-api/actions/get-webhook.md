# Google Dialogflow: Get Webhook

Retrieves a webhook from Google Dialogflow.

```
GET https://connect.mindcloud.co/v1/universal/googleDialogflow/latest/actions/get-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Dialogflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleDialogflow/latest/actions/get-webhook?connectionId=$CONNECTION_ID&name=projects%2Fmy-project%2Flocations%2Fglobal%2Fagents%2Fagent-id%2Fwebhooks%2Fwebhook-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "name": "projects/my-project/locations/global/agents/agent-id/webhooks/webhook-id"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleDialogflow/latest/actions/get-webhook?${params}`, {
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
| `name` | string | yes | Required Dialogflow webhook resource name. Example: `projects/my-project/locations/global/agents/agent-id/webhooks/webhook-id`. |

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

Through the native Google Dialogflow API, this operation is `GET v3/:name` (base URL `https://dialogflow.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-webhook.md) for the provider-specific parameters and requirements.

