# Privy: List Intents

Retrieves a list of intents from Privy.

```
GET https://connect.mindcloud.co/v1/universal/privy/latest/actions/list-intents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Privy `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/privy/latest/actions/list-intents?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/privy/latest/actions/list-intents?${params}`, {
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
      "data": [
        {
          "created_at": 1,
          "created_by_id": "string",
          "expires_at": 1,
          "intent_type": "string",
          "resource_id": "string",
          "status": "string"
        }
      ],
      "next_cursor": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].created_at` | number |  |
| `data[].created_by_id` | string |  |
| `data[].expires_at` | number |  |
| `data[].intent_type` | string |  |
| `data[].resource_id` | string |  |
| `data[].status` | string |  |
| `next_cursor` | string |  |

## Native endpoint

Through the native Privy API, this operation is `GET /v1/intents` (base URL `https://api.privy.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-intents.md) for the provider-specific parameters and requirements.

