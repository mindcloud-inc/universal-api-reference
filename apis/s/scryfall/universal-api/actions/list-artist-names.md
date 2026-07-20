# Scryfall: List Artist Names

Retrieves the artist name catalog from Scryfall.

```
GET https://connect.mindcloud.co/v1/universal/scryfall/latest/actions/list-artist-names
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scryfall `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scryfall/latest/actions/list-artist-names?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scryfall/latest/actions/list-artist-names?${params}`, {
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
        "string"
      ],
      "object": "string",
      "total_values": 1,
      "uri": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<string> |  |
| `object` | string |  |
| `total_values` | number |  |
| `uri` | string |  |

## Native endpoint

Through the native Scryfall API, this operation is `GET catalog/artist-names` (base URL `https://api.scryfall.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-artist-names.md) for the provider-specific parameters and requirements.

