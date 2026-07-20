# HiDrive: Get Share Info

Retrieves share information from HiDrive.

```
GET https://connect.mindcloud.co/v1/universal/hidrive/latest/actions/get-share-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HiDrive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hidrive/latest/actions/get-share-info?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hidrive/latest/actions/get-share-info?${params}`, {
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
| `id` | string | yes | Share ID to inspect. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "has_password": true,
      "is_encrypted": true,
      "logo": {},
      "readable": true,
      "salt": "string",
      "space_available": 1,
      "viewmode": "string",
      "wopi": true,
      "writable": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `has_password` | boolean | Whether the share is password protected. |
| `is_encrypted` | boolean | Whether the share is encrypted. |
| `logo` | object | Custom logo information when available. |
| `readable` | boolean | Whether the share is readable. |
| `salt` | string | Salt value for encrypted shares when available. |
| `space_available` | number | Available writable share space. |
| `viewmode` | string | Single-letter share folder display mode. |
| `wopi` | boolean | Whether Online Office is available. |
| `writable` | boolean | Whether the share is writable. |

## Native endpoint

Through the native HiDrive API, this operation is `GET /share/info` (base URL `https://api.hidrive.strato.com/2.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-share-info.md) for the provider-specific parameters and requirements.

