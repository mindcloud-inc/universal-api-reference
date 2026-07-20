# Soniox: Get file

Retrieves a file from Soniox.

```
GET https://connect.mindcloud.co/v1/universal/soniox/latest/actions/get-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Soniox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/soniox/latest/actions/get-file?connectionId=$CONNECTION_ID&fileId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fileId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/soniox/latest/actions/get-file?${params}`, {
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
| `fileId` | string | yes | Unique identifier of the file. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "clientReferenceId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "filename": "Ava Chen",
      "id": "string",
      "size": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clientReferenceId` | string | Optional client tracking identifier. |
| `createdAt` | date | Creation timestamp. |
| `filename` | string | Stored filename. |
| `id` | string | Unique file identifier. |
| `size` | number | File size in bytes. |

## Native endpoint

Through the native Soniox API, this operation is `GET /files/:file_id` (base URL `https://api.soniox.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-file.md) for the provider-specific parameters and requirements.

