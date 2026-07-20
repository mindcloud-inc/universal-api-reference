# BunnyCDN: Global Search

Searches BunnyCDN resources by search term.

```
GET https://connect.mindcloud.co/v1/universal/bunnyCDN/latest/actions/global-search
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BunnyCDN `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bunnyCDN/latest/actions/global-search?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bunnyCDN/latest/actions/global-search?${params}`, {
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
      "From": 1,
      "Query": "string",
      "SearchResults": [
        {}
      ],
      "Size": 1,
      "Total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `From` | number |  |
| `Query` | string |  |
| `SearchResults` | array<object> |  |
| `Size` | number |  |
| `Total` | number |  |

## Native endpoint

Through the native BunnyCDN API, this operation is `GET /search` (base URL `https://api.bunny.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/global-search.md) for the provider-specific parameters and requirements.

