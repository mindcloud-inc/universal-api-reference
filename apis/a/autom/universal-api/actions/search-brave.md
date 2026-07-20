# Autom: Search Brave

Finds Brave search results in Autom.

```
GET https://connect.mindcloud.co/v1/universal/autom/latest/actions/search-brave
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Autom `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/autom/latest/actions/search-brave?connectionId=$CONNECTION_ID&query=MindCloud" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "MindCloud"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/autom/latest/actions/search-brave?${params}`, {
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
| `query` | string | yes | The Brave query to run. Example: `MindCloud`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `page` | number | no | Result page number to request. Example: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "organicResults": [
        {
          "displayedLink": "https://example.com",
          "domain": "string",
          "link": "https://example.com",
          "position": 1,
          "snippet": "string",
          "snippetMatched": [
            "string"
          ],
          "title": "string"
        }
      ],
      "searchParameters": {
        "engine": "string",
        "page": 1,
        "q": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `organicResults[].displayedLink` | string |  |
| `organicResults[].domain` | string |  |
| `organicResults[].link` | string |  |
| `organicResults[].position` | number |  |
| `organicResults[].snippet` | string |  |
| `organicResults[].snippetMatched[]` | string |  |
| `organicResults[].title` | string |  |
| `searchParameters.engine` | string |  |
| `searchParameters.page` | number |  |
| `searchParameters.q` | string |  |

## Native endpoint

Through the native Autom API, this operation is `GET /v1/brave/search` (base URL `https://api.autom.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-brave.md) for the provider-specific parameters and requirements.

