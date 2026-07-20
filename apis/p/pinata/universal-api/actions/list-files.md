# Pinata: List Files

Retrieves files from Pinata for a selected network.

```
GET https://connect.mindcloud.co/v1/universal/pinata/latest/actions/list-files
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pinata `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pinata/latest/actions/list-files?connectionId=$CONNECTION_ID&limit=25&offset=0&network=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "network": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pinata/latest/actions/list-files?${params}`, {
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
| `network` | string | yes | Network to list files from (`private` or `public`). |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cid": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "expires_at": "2026-05-07T12:00:00.000Z",
      "group_id": "string",
      "id": "string",
      "keyvalues": {},
      "mime_type": "string",
      "name": "Ava Chen",
      "number_of_files": 1,
      "size": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cid` | string | Pinned CID. |
| `created_at` | date | Creation timestamp. |
| `expires_at` | date | Expiration timestamp, when present. |
| `group_id` | string | Owning group ID, when present. |
| `id` | string | Pinata file ID. |
| `keyvalues` | object | Custom key/value metadata. |
| `mime_type` | string | Detected MIME type. |
| `name` | string | File name. |
| `number_of_files` | number | Number of files in the upload. |
| `size` | number | File size in bytes. |

## Native endpoint

Through the native Pinata API, this operation is `GET /v3/files/:network` (base URL `https://api.pinata.cloud`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-files.md) for the provider-specific parameters and requirements.

