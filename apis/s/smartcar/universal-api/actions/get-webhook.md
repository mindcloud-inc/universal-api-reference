# Smartcar: Get Webhook

Retrieves a webhook endpoint from Smartcar.

```
GET https://connect.mindcloud.co/v1/universal/smartcar/latest/actions/get-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Smartcar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartcar/latest/actions/get-webhook?connectionId=$CONNECTION_ID&webhookId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "webhookId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartcar/latest/actions/get-webhook?${params}`, {
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
| `webhookId` | string | yes | The unique identifier for the webhook. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {},
      "id": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes` | object |  |
| `id` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Smartcar API, this operation is `GET https://management.api.smartcar.com/v3/webhooks/:webhookId` (base URL `https://vehicle.api.smartcar.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-webhook.md) for the provider-specific parameters and requirements.

