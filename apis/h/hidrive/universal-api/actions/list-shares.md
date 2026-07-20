# HiDrive: List Shares

Retrieves shares from HiDrive.

```
GET https://connect.mindcloud.co/v1/universal/hidrive/latest/actions/list-shares
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HiDrive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hidrive/latest/actions/list-shares?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hidrive/latest/actions/list-shares?${params}`, {
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
| `fields` | string | no | Comma-separated share fields to include. |
| `id` | string | no | Share ID to retrieve. |
| `path` | string | no | Shared path. |
| `pid` | string | no | Shared path public ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "created": 1,
      "file_type": "string",
      "has_password": true,
      "id": "string",
      "is_encrypted": true,
      "maxcount": 1,
      "path": "string",
      "readable": true,
      "share_type": "string",
      "status": "string",
      "uri": "string",
      "writable": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number | Usage count. |
| `created` | number | Creation timestamp. |
| `file_type` | string | Shared object file type. |
| `has_password` | boolean | Whether the share is password protected. |
| `id` | string | Share ID. |
| `is_encrypted` | boolean | Whether the share is encrypted. |
| `maxcount` | number | Maximum usage count. |
| `path` | string | Shared directory path. |
| `readable` | boolean | Whether the share is readable. |
| `share_type` | string | Type of share. |
| `status` | string | Share status. |
| `uri` | string | Share URI when returned. |
| `writable` | boolean | Whether the share is writable. |

## Native endpoint

Through the native HiDrive API, this operation is `GET /share` (base URL `https://api.hidrive.strato.com/2.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-shares.md) for the provider-specific parameters and requirements.

