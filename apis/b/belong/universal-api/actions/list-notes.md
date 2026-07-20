# Belong: List Notes

Retrieves all note entries from Belong.

```
GET https://connect.mindcloud.co/v1/universal/belong/latest/actions/list-notes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Belong `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/belong/latest/actions/list-notes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/belong/latest/actions/list-notes?${params}`, {
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
| `hubId` | string | no | Example: `64f19d90e9ac7f0f4d86b3f1`. |
| `userId` | string | no | Example: `69d45f6c6e0cc96c27ed7be4`. |
| `search` | string | no | Example: `launch notes`. |
| `take` | number | no | Example: `20`. |
| `skip` | number | no | Example: `0`. |
| `cursor` | string | no | Example: `67f930635a7faf0a41f76f5d`. |
| `sort` | list | no | One of: `Created At`, `Title`, `Updated At`. |
| `order` | list | no | One of: `Ascending`, `Descending`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "hubId": "string",
      "id": "string",
      "title": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content` | string | Note body content. |
| `createdAt` | date | Creation timestamp. |
| `description` | string | Short note description. |
| `hubId` | string | Belong hub ID associated with the note. |
| `id` | string | Belong note ID. |
| `title` | string | Note title. |
| `updatedAt` | date | Last update timestamp. |
| `userId` | string | Owner user ID. |

## Native endpoint

Through the native Belong API, this operation is `GET /notes` (base URL `https://api.belong.net/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-notes.md) for the provider-specific parameters and requirements.

