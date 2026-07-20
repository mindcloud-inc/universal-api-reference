# Cloro: Extract Google AI Overview



```
POST https://connect.mindcloud.co/v1/universal/cloro/latest/actions/extract-google-ai-overview
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cloro/latest/actions/extract-google-ai-overview" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "query": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cloro/latest/actions/extract-google-ai-overview', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "query": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `country` | string | no | ISO 3166-1 alpha-2 country code for localized search results. |
| `query` | string | yes | The search query to execute on Google. |
| `include` | object | no | Optional flags for additional Google response data. |
| `include.aioverview` | object | no | Request Google AI Overview data in the Google Search response. |
| `include.aioverview.markdown` | boolean | no | Include markdown in the AI Overview response object. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": {
        "organicResults": [
          {
            "displayedLink": "https://example.com",
            "link": "https://example.com",
            "page": 1,
            "position": 1,
            "snippet": "string",
            "title": "string"
          }
        ],
        "relatedSearches": [
          {
            "link": "https://example.com",
            "query": "string"
          }
        ]
      },
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result.organicResults[].displayedLink` | string |  |
| `result.organicResults[].link` | string |  |
| `result.organicResults[].page` | number |  |
| `result.organicResults[].position` | number |  |
| `result.organicResults[].snippet` | string |  |
| `result.organicResults[].title` | string |  |
| `result.relatedSearches[].link` | string |  |
| `result.relatedSearches[].query` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Cloro API, this operation is `POST /v1/monitor/google` (base URL `https://api.cloro.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/extract-google-ai-overview.md) for the provider-specific parameters and requirements.

