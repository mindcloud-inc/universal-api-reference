# PrintNode: List Download Clients

Retrieves available client downloads from PrintNode.

```
GET https://connect.mindcloud.co/v1/universal/printNode/latest/actions/list-download-clients
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PrintNode `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/printNode/latest/actions/list-download-clients?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/printNode/latest/actions/list-download-clients?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "edition": "string",
      "enabled": true,
      "filename": "Ava Chen",
      "filesize": 1,
      "id": 1,
      "os": "string",
      "releaseTimestamp": "2026-05-07T12:00:00.000Z",
      "sha1": "string",
      "url": "https://example.com",
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `edition` | string | PrintNode client edition name. |
| `enabled` | boolean | Whether the download is enabled for the edition. |
| `filename` | string | Download filename. |
| `filesize` | number | Download file size in bytes. |
| `id` | number | Download identifier. |
| `os` | string | Supported operating system token. |
| `releaseTimestamp` | date | Release timestamp for the client build. |
| `sha1` | string | SHA1 digest of the client build. |
| `url` | string | Direct download URL for the client build. |
| `version` | string | Client version. |

## Native endpoint

Through the native PrintNode API, this operation is `GET /download/clients` (base URL `https://api.printnode.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-download-clients.md) for the provider-specific parameters and requirements.

