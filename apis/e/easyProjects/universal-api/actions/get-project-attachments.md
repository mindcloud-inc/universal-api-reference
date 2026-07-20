# Easy Projects: Get Project Attachments

Retrieves attachments from a specific Easy Projects project.

```
GET https://connect.mindcloud.co/v1/universal/easyProjects/latest/actions/get-project-attachments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Easy Projects `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/easyProjects/latest/actions/get-project-attachments?connectionId=$CONNECTION_ID&limit=25&offset=0&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/easyProjects/latest/actions/get-project-attachments?${params}`, {
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
| `id` | string | yes | Birdview project ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "canDelete": true,
      "downloadUrl": "https://example.com",
      "externalLink": "https://example.com",
      "fileLength": 1,
      "fileName": "Ava Chen",
      "fileType": "string",
      "hasThumbnail": true,
      "id": 1,
      "messageId": 1,
      "thumbnailUrl": "https://example.com",
      "version": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `canDelete` | boolean |  |
| `downloadUrl` | string |  |
| `externalLink` | string |  |
| `fileLength` | number |  |
| `fileName` | string |  |
| `fileType` | string |  |
| `hasThumbnail` | boolean |  |
| `id` | number |  |
| `messageId` | number |  |
| `thumbnailUrl` | string |  |
| `version` | number |  |

## Native endpoint

Through the native Easy Projects API, this operation is `GET /api/v1/projects/:id/attachments` (base URL `https://api.go.easyprojects.net/api/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-project-attachments.md) for the provider-specific parameters and requirements.

