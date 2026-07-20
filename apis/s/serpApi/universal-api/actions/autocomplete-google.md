# SerpApi: Autocomplete Google

Retrieves Google autocomplete suggestions from SerpApi.

```
GET https://connect.mindcloud.co/v1/universal/serpApi/latest/actions/autocomplete-google
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SerpApi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/serpApi/latest/actions/autocomplete-google?connectionId=$CONNECTION_ID&q=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "q": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/serpApi/latest/actions/autocomplete-google?${params}`, {
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
| `q` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "relevance": 1,
      "serpapiLink": "https://example.com",
      "type": "string",
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `relevance` | number | Provider relevance score for the suggestion. |
| `serpapiLink` | string | SerpApi follow-up link for the suggestion. |
| `type` | string | Suggestion category from SerpApi. |
| `value` | string | Autocomplete suggestion text. |

## Native endpoint

Through the native SerpApi API, this operation is `GET /search.json` (base URL `https://serpapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/autocomplete-google.md) for the provider-specific parameters and requirements.

