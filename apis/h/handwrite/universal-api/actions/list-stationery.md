# Handwrite: List Stationery

Retrieves stationery from Handwrite.

```
GET https://connect.mindcloud.co/v1/universal/handwrite/latest/actions/list-stationery
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Handwrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/handwrite/latest/actions/list-stationery?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/handwrite/latest/actions/list-stationery?${params}`, {
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
      "_id": "string",
      "name": "Ava Chen",
      "preview_url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string | Handwrite stationery ID. |
| `name` | string | Stationery display name. |
| `preview_url` | string | Preview image URL for the stationery. |

## Native endpoint

Through the native Handwrite API, this operation is `GET /stationery` (base URL `https://api.handwrite.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-stationery.md) for the provider-specific parameters and requirements.

