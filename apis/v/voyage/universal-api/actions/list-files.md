# Voyage: List Files

Retrieves files from Voyage.

```
GET https://connect.mindcloud.co/v1/universal/voyage/latest/actions/list-files
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Voyage `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/voyage/latest/actions/list-files?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/voyage/latest/actions/list-files?${params}`, {
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
| `purpose` | string | no | Filter files by purpose. |
| `order` | list | no | Sort order for files by creation time. One of: `0`, `1`. |

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

Through the native Voyage API, this operation is `GET /v1/files` (base URL `https://api.voyageai.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-files.md) for the provider-specific parameters and requirements.

