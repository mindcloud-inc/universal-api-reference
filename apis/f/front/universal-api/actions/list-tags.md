# Front: List Tags

Retrieves a list of tags from Front.

```
GET https://connect.mindcloud.co/v1/universal/front/latest/actions/list-tags
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Front `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/front/latest/actions/list-tags?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/front/latest/actions/list-tags?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sortBy` | list | no | Field used to sort the tags. Front only documents id. One of: `0`. |
| `sortOrder` | list | no | Order by which results should be sorted. One of: `0`, `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": 1,
      "description": {},
      "highlight": "string",
      "id": "string",
      "isPrivate": true,
      "isVisibleInConversationLists": true,
      "links": {
        "related": {
          "children": {},
          "conversations": "https://example.com",
          "owner": "https://example.com",
          "parentTag": {}
        },
        "self": "https://example.com"
      },
      "name": "Ava Chen",
      "updatedAt": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | number |  |
| `description` | object |  |
| `highlight` | string |  |
| `id` | string |  |
| `isPrivate` | boolean |  |
| `isVisibleInConversationLists` | boolean |  |
| `links.related.children` | object |  |
| `links.related.conversations` | string |  |
| `links.related.owner` | string |  |
| `links.related.parentTag` | object |  |
| `links.self` | string |  |
| `name` | string |  |
| `updatedAt` | number |  |

## Native endpoint

Through the native Front API, this operation is `GET /tags` (base URL `https://api2.frontapp.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-tags.md) for the provider-specific parameters and requirements.

