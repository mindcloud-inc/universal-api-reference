# Sapling: List Dictionary Entries

Retrieves custom dictionary entries from Sapling.

```
GET https://connect.mindcloud.co/v1/universal/sapling/latest/actions/list-dictionary-entries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sapling `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sapling/latest/actions/list-dictionary-entries?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sapling/latest/actions/list-dictionary-entries?${params}`, {
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
      "created_at": "string",
      "entry": "string",
      "id": "string",
      "updated_at": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | string |  |
| `entry` | string |  |
| `id` | string |  |
| `updated_at` | string |  |

## Native endpoint

Through the native Sapling API, this operation is `GET /api/v1/dictionary` (base URL `https://api.sapling.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-dictionary-entries.md) for the provider-specific parameters and requirements.

