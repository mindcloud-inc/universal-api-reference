# folk: List Notes

Retrieves a list of notes from folk.

```
GET https://connect.mindcloud.co/v1/universal/folk/latest/actions/list-notes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a folk `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/folk/latest/actions/list-notes?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/folk/latest/actions/list-notes?${params}`, {
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
| `entityId` | string | no | Filter notes by entity. Only notes linked to the specified entity will be returned. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "author": {},
      "content": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "entity": {},
      "id": "string",
      "parentNote": {},
      "visibility": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `author` | object |  |
| `content` | string |  |
| `createdAt` | date |  |
| `entity` | object |  |
| `id` | string |  |
| `parentNote` | object |  |
| `visibility` | string |  |

## Native endpoint

Through the native folk API, this operation is `GET /v1/notes` (base URL `https://api.folk.app`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-notes.md) for the provider-specific parameters and requirements.

