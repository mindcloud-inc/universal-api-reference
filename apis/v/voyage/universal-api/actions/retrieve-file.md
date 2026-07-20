# Voyage: Retrieve File

Retrieves a file from Voyage.

```
GET https://connect.mindcloud.co/v1/universal/voyage/latest/actions/retrieve-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Voyage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/voyage/latest/actions/retrieve-file?connectionId=$CONNECTION_ID&fileId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fileId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/voyage/latest/actions/retrieve-file?${params}`, {
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
| `fileId` | string | yes | ID of the file to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bytes": 1,
      "createdAt": "string",
      "expiresAt": "string",
      "filename": "Ava Chen",
      "id": "string",
      "object": "string",
      "purpose": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bytes` | number | File size in bytes. |
| `createdAt` | string | File creation timestamp. |
| `expiresAt` | string | File expiration timestamp. |
| `filename` | string | Stored filename. |
| `id` | string | Voyage file ID. |
| `object` | string | Object type for the file. |
| `purpose` | string | Configured file purpose. |

## Native endpoint

Through the native Voyage API, this operation is `GET /v1/files/:fileId` (base URL `https://api.voyageai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-file.md) for the provider-specific parameters and requirements.

