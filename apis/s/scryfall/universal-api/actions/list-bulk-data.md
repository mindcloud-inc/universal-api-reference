# Scryfall: List Bulk Data

Retrieves bulk data records from Scryfall.

```
GET https://connect.mindcloud.co/v1/universal/scryfall/latest/actions/list-bulk-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scryfall `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scryfall/latest/actions/list-bulk-data?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scryfall/latest/actions/list-bulk-data?${params}`, {
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
      "description": "string",
      "download_uri": "string",
      "id": "string",
      "name": "Ava Chen",
      "size": 1,
      "type": "string",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `download_uri` | string |  |
| `id` | string |  |
| `name` | string |  |
| `size` | number |  |
| `type` | string |  |
| `updated_at` | date |  |

## Native endpoint

Through the native Scryfall API, this operation is `GET bulk-data` (base URL `https://api.scryfall.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-bulk-data.md) for the provider-specific parameters and requirements.

