# Customer.io: Get Broadcast

Retrieves a broadcast from Customer.io.

```
GET https://connect.mindcloud.co/v1/universal/customerio/latest/actions/get-broadcast
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Customer.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/customerio/latest/actions/get-broadcast?connectionId=$CONNECTION_ID&broadcastId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "broadcastId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/customerio/latest/actions/get-broadcast?${params}`, {
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
| `broadcastId` | number | yes | The numeric ID of the broadcast you want to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "actions": [
        {}
      ],
      "active": true,
      "created": 1,
      "deduplicateId": "string",
      "firstStarted": 1,
      "id": 1,
      "name": "Ava Chen",
      "state": "string",
      "tags": [
        "string"
      ],
      "type": "string",
      "updated": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actions` | array<object> | The actions configured in the broadcast. |
| `active` | boolean | Whether the broadcast is active. |
| `created` | number | Unix timestamp when the broadcast was created. |
| `deduplicateId` | string | The deduplication token for the broadcast. |
| `firstStarted` | number | Unix timestamp when the broadcast first started. |
| `id` | number | The identifier for the broadcast. |
| `name` | string | The name of the broadcast. |
| `state` | string | The broadcast state. |
| `tags` | array<string> | Tags applied to the broadcast. |
| `type` | string | The broadcast type. |
| `updated` | number | Unix timestamp when the broadcast was last updated. |

## Native endpoint

Through the native Customer.io API, this operation is `GET /v1/broadcasts/:broadcast_id` (base URL `https://api.customer.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-broadcast.md) for the provider-specific parameters and requirements.

