# Cat Facts: List Facts



```
GET https://connect.mindcloud.co/v1/universal/catFacts/latest/actions/list-facts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cat Facts `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/catFacts/latest/actions/list-facts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/catFacts/latest/actions/list-facts?${params}`, {
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
| `max_length` | number | no | Maximum length of each returned fact. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "current_page": 1,
      "data": [
        {
          "fact": "string",
          "length": 1
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
| `data` | array<object> | Cat facts for the current page. |
| `data[].fact` | string | Cat fact text. |
| `data[].length` | number | Length of the fact. |
| `next_page_url` | string | URL for the next page, when available. |
| `per_page` | number | Number of facts returned per page. |
| `total` | number | Total available facts. |

## Native endpoint

Through the native Cat Facts API, this operation is `GET /facts` (base URL `https://catfact.ninja`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-facts.md) for the provider-specific parameters and requirements.

