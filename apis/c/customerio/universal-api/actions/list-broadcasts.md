# Customer.io: List Broadcasts

Retrieves broadcasts from Customer.io.

```
GET https://connect.mindcloud.co/v1/universal/customerio/latest/actions/list-broadcasts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Customer.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/customerio/latest/actions/list-broadcasts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/customerio/latest/actions/list-broadcasts?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



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

Through the native Customer.io API, this operation is `GET /v1/broadcasts` (base URL `https://api.customer.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-broadcasts.md) for the provider-specific parameters and requirements.

