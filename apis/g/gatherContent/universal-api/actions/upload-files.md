# GatherContent: Upload Files

Uploads a file to a GatherContent project.

```
POST https://connect.mindcloud.co/v1/universal/gatherContent/latest/actions/upload-files
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GatherContent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/gatherContent/latest/actions/upload-files" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "string",
  "project_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gatherContent/latest/actions/upload-files', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file": "string",
    "project_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `file` | file | yes | File upload payload. |
| `project_id` | string | yes | Project id. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "download_url": "https://example.com",
      "filename": "Ava Chen",
      "id": "string",
      "mime_type": "string",
      "project_id": 1,
      "size": 1,
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `download_url` | string |  |
| `filename` | string |  |
| `id` | string |  |
| `mime_type` | string |  |
| `project_id` | number |  |
| `size` | number |  |
| `url` | string |  |

## Native endpoint

Through the native GatherContent API, this operation is `POST /projects/:project_id/files` (base URL `https://api.gathercontent.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-files.md) for the provider-specific parameters and requirements.

