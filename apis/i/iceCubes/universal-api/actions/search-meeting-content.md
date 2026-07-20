# IceCubes: Search Meeting Content



```
GET https://connect.mindcloud.co/v1/universal/iceCubes/latest/actions/search-meeting-content
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a IceCubes `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iceCubes/latest/actions/search-meeting-content?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iceCubes/latest/actions/search-meeting-content?${params}`, {
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
| `query` | string | yes | Search query across meeting content. |
| `contentType` | string | no | Filter by content type. |
| `speaker` | string | no | Filter by speaker name. |
| `tag` | string | no | Filter by tag name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "pagination": {},
      "results": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `pagination` | object | Pagination metadata for the search results. |
| `results` | array<object> | Search results across meeting content. |

## Native endpoint

Through the native IceCubes API, this operation is `GET /search` (base URL `https://icecubes.app/api/public`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-meeting-content.md) for the provider-specific parameters and requirements.

