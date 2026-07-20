# ScrapingDog: Autocomplete Google

Retrieves Google autocomplete suggestions through ScrapingDog.

```
GET https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/autocomplete-google
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScrapingDog `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/autocomplete-google?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/autocomplete-google?${params}`, {
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
| `query` | string | yes | Search query for Google autocomplete suggestions. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "suggestions": {
        "relevance": 1,
        "type": "string",
        "value": "string"
      },
      "verbatim_relevance": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `suggestions` | array<object> |  |
| `suggestions.relevance` | number |  |
| `suggestions.type` | string |  |
| `suggestions.value` | string |  |
| `verbatim_relevance` | number |  |

## Native endpoint

Through the native ScrapingDog API, this operation is `GET /google_autocomplete` (base URL `https://api.scrapingdog.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/autocomplete-google.md) for the provider-specific parameters and requirements.

