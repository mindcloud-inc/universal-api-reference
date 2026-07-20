# Manus: Get File

Retrieves a file from Manus by ID.

```
GET https://connect.mindcloud.co/v1/universal/manus/latest/actions/get-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Manus `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/manus/latest/actions/get-file?connectionId=$CONNECTION_ID&fileId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fileId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/manus/latest/actions/get-file?${params}`, {
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
| `fileId` | string | yes | The ID of the file to retrieve |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "expiresAt": "string",
      "filename": "Ava Chen",
      "id": "string",
      "object": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `expiresAt` | string |  |
| `filename` | string |  |
| `id` | string |  |
| `object` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Manus API, this operation is `GET /files/:file_id` (base URL `https://api.manus.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-file.md) for the provider-specific parameters and requirements.

