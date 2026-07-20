# HiDrive: Get File Hashes

Retrieves file hashes from HiDrive.

```
GET https://connect.mindcloud.co/v1/universal/hidrive/latest/actions/get-file-hashes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HiDrive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hidrive/latest/actions/get-file-hashes?connectionId=$CONNECTION_ID&level=1&ranges=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "level": "1",
  "ranges": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hidrive/latest/actions/get-file-hashes?${params}`, {
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
| `path` | string | no | File path. |
| `pid` | string | no | File public ID. |
| `level` | number | yes | Hash level requested. |
| `ranges` | string | yes | Comma-separated byte ranges. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "chash": "string",
      "level": 1,
      "list": [
        [
          "string"
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `chash` | string | Content hash for the requested range set. |
| `level` | number | Hash tree level. |
| `list` | array<array> | Hash entries per requested range. |

## Native endpoint

Through the native HiDrive API, this operation is `GET /file/hash` (base URL `https://api.hidrive.strato.com/2.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-file-hashes.md) for the provider-specific parameters and requirements.

