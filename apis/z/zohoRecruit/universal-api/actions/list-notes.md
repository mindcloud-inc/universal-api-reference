# Zoho Recruit: List Notes

Retrieves all notes from Zoho Recruit.

```
GET https://connect.mindcloud.co/v1/universal/zohoRecruit/latest/actions/list-notes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Recruit `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoRecruit/latest/actions/list-notes?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoRecruit/latest/actions/list-notes?${params}`, {
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
| `page` | number | no | Page number of notes to fetch. |
| `perPage` | number | no | Maximum number of notes to fetch per page. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdBy": {},
      "createdTime": "string",
      "id": "string",
      "modifiedBy": {},
      "modifiedTime": "string",
      "noteContent": "string",
      "noteOwner": {},
      "noteTitle": "string",
      "parentId": {},
      "seModule": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdBy` | object |  |
| `createdTime` | string |  |
| `id` | string |  |
| `modifiedBy` | object |  |
| `modifiedTime` | string |  |
| `noteContent` | string |  |
| `noteOwner` | object |  |
| `noteTitle` | string |  |
| `parentId` | object |  |
| `seModule` | string |  |

## Native endpoint

Through the native Zoho Recruit API, this operation is `GET /Notes` (base URL `https://recruit.zoho.com/recruit/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-notes.md) for the provider-specific parameters and requirements.

