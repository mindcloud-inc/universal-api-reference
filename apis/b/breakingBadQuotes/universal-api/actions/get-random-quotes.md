# Breaking Bad Quotes: Get Random Quotes



```
GET https://connect.mindcloud.co/v1/universal/breakingBadQuotes/latest/actions/get-random-quotes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Breaking Bad Quotes `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/breakingBadQuotes/latest/actions/get-random-quotes?connectionId=$CONNECTION_ID&count=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "count": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/breakingBadQuotes/latest/actions/get-random-quotes?${params}`, {
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
| `count` | number | yes | Positive whole-number count of unique random quotes. The current first-party corpus caps requests at 174 quotes. |

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

Through the native Breaking Bad Quotes API, this operation is `GET /v1/quotes/:count` (base URL `https://api.breakingbadquotes.xyz`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-random-quotes.md) for the provider-specific parameters and requirements.

