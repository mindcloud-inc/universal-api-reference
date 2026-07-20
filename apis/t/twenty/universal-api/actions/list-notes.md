# Twenty: List Notes



```
GET https://connect.mindcloud.co/v1/universal/twenty/latest/actions/list-notes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Twenty `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/twenty/latest/actions/list-notes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/twenty/latest/actions/list-notes?${params}`, {
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
      "bodyV2": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": {
        "name": "Ava Chen",
        "source": "string"
      },
      "deletedAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "position": 1,
      "searchVector": "string",
      "title": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "updatedBy": {
        "name": "Ava Chen",
        "source": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bodyV2` | string |  |
| `createdAt` | date |  |
| `createdBy.name` | string |  |
| `createdBy.source` | string |  |
| `deletedAt` | date |  |
| `id` | string |  |
| `position` | number |  |
| `searchVector` | string |  |
| `title` | string |  |
| `updatedAt` | date |  |
| `updatedBy.name` | string |  |
| `updatedBy.source` | string |  |

## Native endpoint

Through the native Twenty API, this operation is `GET /rest/notes` (base URL `https://api.twenty.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-notes.md) for the provider-specific parameters and requirements.

