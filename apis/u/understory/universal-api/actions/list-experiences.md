# Understory: List Experiences

Retrieves experiences from Understory.

```
GET https://connect.mindcloud.co/v1/universal/understory/latest/actions/list-experiences
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Understory `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/understory/latest/actions/list-experiences?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/understory/latest/actions/list-experiences?${params}`, {
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
      "items": [
        {
          "created_at": "2026-05-07T12:00:00.000Z",
          "description": "string",
          "id": "string",
          "media": [
            {
              "mime_type": "string",
              "type": "string",
              "url": "https://example.com"
            }
          ],
          "name": "Ava Chen",
          "state": "string",
          "tag_ids": [
            [
              "string"
            ]
          ],
          "type": "string",
          "updated_at": "2026-05-07T12:00:00.000Z"
        }
      ],
      "next": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `items[].created_at` | date |  |
| `items[].description` | string |  |
| `items[].id` | string |  |
| `items[].media[].mime_type` | string |  |
| `items[].media[].type` | string |  |
| `items[].media[].url` | string |  |
| `items[].name` | string |  |
| `items[].state` | string |  |
| `items[].tag_ids[]` | array<string> |  |
| `items[].type` | string |  |
| `items[].updated_at` | date |  |
| `next` | string |  |

## Native endpoint

Through the native Understory API, this operation is `GET /v1/experiences` (base URL `https://api.understory.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-experiences.md) for the provider-specific parameters and requirements.

