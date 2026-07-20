# Olostep: Create Map

Creates a new map in Olostep.

```
POST https://connect.mindcloud.co/v1/universal/olostep/latest/actions/create-map
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Olostep `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/olostep/latest/actions/create-map" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/olostep/latest/actions/create-map', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | yes | The website URL to map. Example: `https://example.com`. |
| `searchQuery` | string | no | Optional search query to sort map URLs by relevance. Example: `api reference docs`. |
| `topN` | number | no | Optional number of top URLs to return for a search query. Example: `25`. |
| `includeSubdomain` | boolean | no | Whether to include subdomains of the given URL. Example: `true`. |
| `includeUrls[]` | array<string> | no | Optional glob patterns of URL paths to include. Accepts multiple values as an array. Example: `/docs/**`. |
| `excludeUrls[]` | array<string> | no | Optional glob patterns of URL paths to exclude. Accepts multiple values as an array. Example: `/blog/**`. |
| `cursor` | string | no | Optional pagination cursor from a previous map response. Example: `next_cursor_token`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "urls": [
        "https://example.com"
      ],
      "urlsCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `urls[]` | string |  |
| `urlsCount` | number |  |

## Native endpoint

Through the native Olostep API, this operation is `POST /v1/maps` (base URL `https://api.olostep.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-map.md) for the provider-specific parameters and requirements.

