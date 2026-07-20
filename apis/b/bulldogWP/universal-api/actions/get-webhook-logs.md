# Bulldog-WP: Get webhook logs

Retrieves webhook logs from Bulldog-WP.

```
GET https://connect.mindcloud.co/v1/universal/bulldogWP/latest/actions/get-webhook-logs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bulldog-WP `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bulldogWP/latest/actions/get-webhook-logs?connectionId=$CONNECTION_ID&limit=25&offset=0&webhookId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "webhookId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bulldogWP/latest/actions/get-webhook-logs?${params}`, {
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
      "body": "string",
      "code": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "deviceId": "string",
      "event": "string",
      "id": "string",
      "message": "string",
      "objectEvent": "string",
      "objectId": "string",
      "objectType": "string",
      "responseTime": 1,
      "webhook": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `body` | string |  |
| `code` | string |  |
| `createdAt` | date |  |
| `deviceId` | string |  |
| `event` | string |  |
| `id` | string |  |
| `message` | string |  |
| `objectEvent` | string |  |
| `objectId` | string |  |
| `objectType` | string |  |
| `responseTime` | number |  |
| `webhook` | object |  |

## Native endpoint

Through the native Bulldog-WP API, this operation is `GET /webhooks/{webhookId}/logs` (base URL `https://api.bulldog-wp.co.il/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-webhook-logs.md) for the provider-specific parameters and requirements.

