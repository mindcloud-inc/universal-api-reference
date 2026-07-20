# Piloterr: Search Google



```
GET https://connect.mindcloud.co/v1/universal/piloterr/latest/actions/search-google
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Piloterr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/piloterr/latest/actions/search-google?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/piloterr/latest/actions/search-google?${params}`, {
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
| `gl` | string | no | Two-letter Google country code. |
| `hl` | string | no | Two-letter Google language code. |
| `query` | string | yes | Google search query. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "organicResults": {
        "link": "https://example.com",
        "title": "string"
      },
      "searchInformation": {
        "totalResults": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `organicResults.link` | string |  |
| `organicResults.title` | string |  |
| `searchInformation.totalResults` | string |  |

## Native endpoint

Through the native Piloterr API, this operation is `GET /google/search` (base URL `https://api.piloterr.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-google.md) for the provider-specific parameters and requirements.

