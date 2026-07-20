# Locu: List Webhook Deliveries

Retrieves recent webhook deliveries from Locu.

```
GET https://connect.mindcloud.co/v1/universal/locu/latest/actions/list-webhook-deliveries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Locu `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/locu/latest/actions/list-webhook-deliveries?connectionId=$CONNECTION_ID&limit=25&offset=0&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/locu/latest/actions/list-webhook-deliveries?${params}`, {
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
| `id` | string | yes | Webhook ID to list deliveries for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attemptNumber": 1,
      "completedAt": "2026-05-07T12:00:00.000Z",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "errorMessage": "string",
      "id": "string",
      "responseStatus": 1,
      "status": "string",
      "webhookId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attemptNumber` | number |  |
| `completedAt` | date |  |
| `createdAt` | date |  |
| `errorMessage` | string |  |
| `id` | string |  |
| `responseStatus` | number |  |
| `status` | string |  |
| `webhookId` | string |  |

## Native endpoint

Through the native Locu API, this operation is `GET /webhooks/:id/deliveries` (base URL `https://api.locu.app/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-webhook-deliveries.md) for the provider-specific parameters and requirements.

