# Breaking Bad Quotes: Get Random Quote



```
GET https://connect.mindcloud.co/v1/universal/breakingBadQuotes/latest/actions/get-random-quote
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Breaking Bad Quotes `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/breakingBadQuotes/latest/actions/get-random-quote?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/breakingBadQuotes/latest/actions/get-random-quote?${params}`, {
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
      "author": "string",
      "quote": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `author` | string | Quote author as supplied by the provider. |
| `quote` | string | Quote text as supplied by the provider. |

## Native endpoint

Through the native Breaking Bad Quotes API, this operation is `GET /v1/quotes` (base URL `https://api.breakingbadquotes.xyz`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-random-quote.md) for the provider-specific parameters and requirements.

