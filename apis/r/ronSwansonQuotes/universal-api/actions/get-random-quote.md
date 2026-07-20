# Ron Swanson Quotes: Get Random Quote

Retrieves a random Ron Swanson quote.

```
GET https://connect.mindcloud.co/v1/universal/ronSwansonQuotes/latest/actions/get-random-quote
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ron Swanson Quotes `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ronSwansonQuotes/latest/actions/get-random-quote?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ronSwansonQuotes/latest/actions/get-random-quote?${params}`, {
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
      "quote": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `quote` | string | Ron Swanson quote text. |

## Native endpoint

Through the native Ron Swanson Quotes API, this operation is `GET /quotes` (base URL `https://ron-swanson-quotes.herokuapp.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-random-quote.md) for the provider-specific parameters and requirements.

