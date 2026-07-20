# ProdPad: List Ideas

Retrieves ideas from ProdPad.

```
GET https://connect.mindcloud.co/v1/universal/prodPad/latest/actions/list-ideas
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProdPad `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/prodPad/latest/actions/list-ideas?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/prodPad/latest/actions/list-ideas?${params}`, {
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
| `tags` | string | no | Accepts multiple values in one string, delimited by `,`. |
| `product` | string | no |  |
| `persona` | string | no |  |
| `status` | string | no |  |
| `state` | string | no |  |
| `externalId` | string | no |  |
| `externalUrl` | string | no |  |
| `withFeedback` | boolean | no | Return associated feedback with each idea. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "idea_count": 1,
      "ideas": [
        {
          "account": {
            "id": 1,
            "name": "Ava Chen",
            "slug": "string"
          },
          "actual_outcomes": "string",
          "confidence": "string",
          "created_at": "2026-05-07T12:00:00.000Z",
          "creator": {
            "display_name": "Ava Chen",
            "id": 1,
            "username": "Ava Chen"
          },
          "description": "string",
          "engagement": 1,
          "id": 1,
          "impact": 1,
          "popularity": 1,
          "project_id": 1,
          "state": "string",
          "target_outcomes": "string",
          "title": "string",
          "updated_at": "2026-05-07T12:00:00.000Z",
          "uuid": "string",
          "web_url": "https://example.com"
        }
      ],
      "page": 1,
      "size": 1,
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `idea_count` | number |  |
| `ideas[].account.id` | number |  |
| `ideas[].account.name` | string |  |
| `ideas[].account.slug` | string |  |
| `ideas[].actual_outcomes` | string |  |
| `ideas[].confidence` | string |  |
| `ideas[].created_at` | date |  |
| `ideas[].creator.display_name` | string |  |
| `ideas[].creator.id` | number |  |
| `ideas[].creator.username` | string |  |
| `ideas[].description` | string |  |
| `ideas[].engagement` | number |  |
| `ideas[].id` | number |  |
| `ideas[].impact` | number |  |
| `ideas[].popularity` | number |  |
| `ideas[].project_id` | number |  |
| `ideas[].state` | string |  |
| `ideas[].target_outcomes` | string |  |
| `ideas[].title` | string |  |
| `ideas[].updated_at` | date |  |
| `ideas[].uuid` | string |  |
| `ideas[].web_url` | string |  |
| `page` | number |  |
| `size` | number |  |
| `success` | boolean |  |

## Native endpoint

Through the native ProdPad API, this operation is `GET /ideas` (base URL `https://api.prodpad.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-ideas.md) for the provider-specific parameters and requirements.

