# Bulldog-WP: Get webhook details

Retrieves a webhook from Bulldog-WP.

```
GET https://connect.mindcloud.co/v1/universal/bulldogWP/latest/actions/get-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bulldog-WP `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bulldogWP/latest/actions/get-webhook?connectionId=$CONNECTION_ID&webhookId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "webhookId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bulldogWP/latest/actions/get-webhook?${params}`, {
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
| `webhookId` | string | yes | Webhook endpoint ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "device": {},
      "id": "string",
      "lastFailureAt": "2026-05-07T12:00:00.000Z",
      "lastRetryAt": "2026-05-07T12:00:00.000Z",
      "lastRunAt": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "retries": 1,
      "status": 1,
      "url": "https://example.com",
      "user": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `device` | object |  |
| `id` | string |  |
| `lastFailureAt` | date |  |
| `lastRetryAt` | date |  |
| `lastRunAt` | date |  |
| `name` | string |  |
| `retries` | number |  |
| `status` | number |  |
| `url` | string |  |
| `user` | object |  |

## Native endpoint

Through the native Bulldog-WP API, this operation is `GET /webhooks/{webhookId}` (base URL `https://api.bulldog-wp.co.il/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-webhook.md) for the provider-specific parameters and requirements.

