# GatherContent: Get File

Retrieves a file from GatherContent.

```
GET https://connect.mindcloud.co/v1/universal/gatherContent/latest/actions/get-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GatherContent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gatherContent/latest/actions/get-file?connectionId=$CONNECTION_ID&file_id=string&project_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "file_id": "string",
  "project_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gatherContent/latest/actions/get-file?${params}`, {
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
| `file_id` | string | yes | File ID. |
| `project_id` | string | yes | Project ID. |

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

Through the native GatherContent API, this operation is `GET /projects/:project_id/files/:file_id` (base URL `https://api.gathercontent.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-file.md) for the provider-specific parameters and requirements.

