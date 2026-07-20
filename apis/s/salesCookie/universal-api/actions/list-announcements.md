# Sales Cookie: List Announcements

Retrieves workspace announcements from Sales Cookie.

```
GET https://connect.mindcloud.co/v1/universal/salesCookie/latest/actions/list-announcements
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sales Cookie `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/salesCookie/latest/actions/list-announcements?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/salesCookie/latest/actions/list-announcements?${params}`, {
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
      "created": "2026-05-07T12:00:00.000Z",
      "createdById": "string",
      "htmlBody": "string",
      "id": "string",
      "isDeleted": true,
      "level": "string",
      "order": 1,
      "tag": "string",
      "tags": "string",
      "targetId": "string",
      "updated": "2026-05-07T12:00:00.000Z",
      "updatedById": "string",
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | date |  |
| `createdById` | string |  |
| `htmlBody` | string |  |
| `id` | string |  |
| `isDeleted` | boolean |  |
| `level` | string |  |
| `order` | number |  |
| `tag` | string |  |
| `tags` | string |  |
| `targetId` | string |  |
| `updated` | date |  |
| `updatedById` | string |  |
| `workspaceId` | string |  |

## Native endpoint

Through the native Sales Cookie API, this operation is `GET /odata/:apiKey/Announcement` (base URL `https://salescookie.com/app`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-announcements.md) for the provider-specific parameters and requirements.

