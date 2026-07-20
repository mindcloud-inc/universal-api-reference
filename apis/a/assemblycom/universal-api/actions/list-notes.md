# Assembly.com: List Notes

Retrieves notes from Assembly.com.

```
GET https://connect.mindcloud.co/v1/universal/assemblycom/latest/actions/list-notes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Assembly.com `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/assemblycom/latest/actions/list-notes?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/assemblycom/latest/actions/list-notes?${params}`, {
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
| `entityId` | string | no | Only return notes for the entity specified by this ID. |
| `entityType` | string | no | Only return notes that have an entity type matching this value. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "content": "string",
          "createdAt": "2026-05-07T12:00:00.000Z",
          "creatorId": "string",
          "entityId": "string",
          "entityType": "string",
          "id": "string",
          "object": "string",
          "title": "string",
          "updatedAt": "2026-05-07T12:00:00.000Z"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].content` | string |  |
| `data[].createdAt` | date |  |
| `data[].creatorId` | string |  |
| `data[].entityId` | string |  |
| `data[].entityType` | string |  |
| `data[].id` | string |  |
| `data[].object` | string |  |
| `data[].title` | string |  |
| `data[].updatedAt` | date |  |

## Native endpoint

Through the native Assembly.com API, this operation is `GET /notes` (base URL `https://api.assembly.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-notes.md) for the provider-specific parameters and requirements.

