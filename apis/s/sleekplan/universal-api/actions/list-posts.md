# Sleekplan: List Posts



```
GET https://connect.mindcloud.co/v1/universal/sleekplan/latest/actions/list-posts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sleekplan `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sleekplan/latest/actions/list-posts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sleekplan/latest/actions/list-posts?${params}`, {
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
| `advanced` | string | no |  |
| `filter` | string | no |  |
| `owner` | number | no |  |
| `search` | string | no |  |
| `segment` | string | no |  |
| `sort` | string | no |  |
| `tags` | string | no |  |
| `type` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "canDelete": true,
      "canEdit": true,
      "created": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "feedbackId": 1,
      "productId": 1,
      "status": "string",
      "title": "string",
      "totalComments": 1,
      "totalDown": 1,
      "totalUp": 1,
      "type": "string",
      "updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `canDelete` | boolean |  |
| `canEdit` | boolean |  |
| `created` | date |  |
| `description` | string |  |
| `feedbackId` | number |  |
| `productId` | number |  |
| `status` | string |  |
| `title` | string |  |
| `totalComments` | number |  |
| `totalDown` | number |  |
| `totalUp` | number |  |
| `type` | string |  |
| `updated` | date |  |

## Native endpoint

Through the native Sleekplan API, this operation is `GET /posts` (base URL `https://api.sleekplan.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-posts.md) for the provider-specific parameters and requirements.

