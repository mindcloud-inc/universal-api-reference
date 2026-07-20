# 1Shot: List Webhook Endpoints

Retrieves webhook endpoint configurations from 1Shot API.

```
GET https://connect.mindcloud.co/v1/universal/oneShot/latest/actions/list-webhook-endpoints
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 1Shot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oneShot/latest/actions/list-webhook-endpoints?connectionId=$CONNECTION_ID&businessId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "businessId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oneShot/latest/actions/list-webhook-endpoints?${params}`, {
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
| `businessId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "businessId": "string",
      "created": 1,
      "deleted": true,
      "description": "string",
      "destinationUrl": "https://example.com",
      "id": "string",
      "lastPing": 1,
      "lastPingStatus": true,
      "name": "Ava Chen",
      "publicKey": "string",
      "updated": 1,
      "userId": "string",
      "verified": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `businessId` | string |  |
| `created` | number |  |
| `deleted` | boolean |  |
| `description` | string |  |
| `destinationUrl` | string |  |
| `id` | string |  |
| `lastPing` | number |  |
| `lastPingStatus` | boolean |  |
| `name` | string |  |
| `publicKey` | string |  |
| `updated` | number |  |
| `userId` | string |  |
| `verified` | boolean |  |

## Native endpoint

Through the native 1Shot API, this operation is `GET /business/:businessId/webhooks/endpoints` (base URL `https://api.1shotapi.com/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-webhook-endpoints.md) for the provider-specific parameters and requirements.

