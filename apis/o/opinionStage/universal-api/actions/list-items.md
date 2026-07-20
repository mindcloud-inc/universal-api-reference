# Opinion Stage: List Items

Retrieves a list of items from Opinion Stage.

```
GET https://connect.mindcloud.co/v1/universal/opinionStage/latest/actions/list-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Opinion Stage `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/opinionStage/latest/actions/list-items?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/opinionStage/latest/actions/list-items?${params}`, {
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
      "attributes": {
        "embed": {
          "iframe": "string",
          "script": "string"
        },
        "status": "string",
        "timestamps": {
          "created": "2026-05-07T12:00:00.000Z",
          "modified": "2026-05-07T12:00:00.000Z"
        },
        "title": "string"
      },
      "id": "string",
      "links": {
        "edit": "https://example.com",
        "iframe": "https://example.com",
        "landing": "https://example.com",
        "results": "https://example.com",
        "self": "https://example.com"
      },
      "relationships": {
        "questions": {
          "links": {
            "related": "https://example.com"
          }
        }
      },
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.embed.iframe` | string |  |
| `attributes.embed.script` | string |  |
| `attributes.status` | string |  |
| `attributes.timestamps.created` | date |  |
| `attributes.timestamps.modified` | date |  |
| `attributes.title` | string |  |
| `id` | string |  |
| `links.edit` | string |  |
| `links.iframe` | string |  |
| `links.landing` | string |  |
| `links.results` | string |  |
| `links.self` | string |  |
| `relationships.questions.links.related` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Opinion Stage API, this operation is `GET /api/v2/items` (base URL `https://api.opinionstage.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-items.md) for the provider-specific parameters and requirements.

