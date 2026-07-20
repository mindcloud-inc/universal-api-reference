# OPN: Get Event

Retrieves details for an event from OPN.

```
GET https://connect.mindcloud.co/v1/universal/oPN/latest/actions/get-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OPN `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oPN/latest/actions/get-event?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oPN/latest/actions/get-event?${params}`, {
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
| `id` | string | yes | The event ID to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "actor_uid": "string",
      "created_at": "string",
      "data": {},
      "id": "string",
      "key": "string",
      "livemode": true,
      "location": "string",
      "object": "string",
      "team_uid": "string",
      "user_uid": "string",
      "webhook_deliveries": [
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
| `actor_uid` | string |  |
| `created_at` | string |  |
| `data` | object |  |
| `id` | string |  |
| `key` | string |  |
| `livemode` | boolean |  |
| `location` | string |  |
| `object` | string |  |
| `team_uid` | string |  |
| `user_uid` | string |  |
| `webhook_deliveries` | array<object> |  |

## Native endpoint

Through the native OPN API, this operation is `GET /events/:id` (base URL `https://api.omise.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-event.md) for the provider-specific parameters and requirements.

