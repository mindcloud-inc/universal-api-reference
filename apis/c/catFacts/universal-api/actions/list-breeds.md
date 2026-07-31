# Cat Facts: List Breeds



```
GET https://connect.mindcloud.co/v1/universal/catFacts/latest/actions/list-breeds
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cat Facts `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/catFacts/latest/actions/list-breeds?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/catFacts/latest/actions/list-breeds?${params}`, {
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
      "current_page": 1,
      "data": [
        {
          "breed": "string",
          "coat": "string",
          "country": "string",
          "origin": "string",
          "pattern": "string"
        }
      ],
      "next_page_url": "https://example.com",
      "per_page": 1,
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `current_page` | number | Current page number. |
| `data` | array<object> | Cat breeds for the current page. |
| `data[].breed` | string | Breed name. |
| `data[].coat` | string | Coat type. |
| `data[].country` | string | Country associated with the breed. |
| `data[].origin` | string | Breed origin classification. |
| `data[].pattern` | string | Coat pattern. |
| `next_page_url` | string | URL for the next page, when available. |
| `per_page` | number | Number of breeds returned per page. |
| `total` | number | Total available breeds. |

## Native endpoint

Through the native Cat Facts API, this operation is `GET /breeds` (base URL `https://catfact.ninja`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-breeds.md) for the provider-specific parameters and requirements.

