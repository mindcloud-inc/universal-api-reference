# HiDrive: List Mail Uploads

Retrieves mail uploads from HiDrive.

```
GET https://connect.mindcloud.co/v1/universal/hidrive/latest/actions/list-mail-uploads
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HiDrive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hidrive/latest/actions/list-mail-uploads?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hidrive/latest/actions/list-mail-uploads?${params}`, {
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
| `path` | string | no | Directory path for the mail upload. |
| `pid` | string | no | Directory public ID for the mail upload. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "overwrite": true,
      "path": "string",
      "pid": "string",
      "rcpt": "string",
      "reportok": true,
      "reportto": "string",
      "status": "string",
      "subfolder": true,
      "ttl": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `overwrite` | boolean | Whether upload overwrites are enabled. |
| `path` | string | Directory path. |
| `pid` | string | Directory object ID. |
| `rcpt` | string | Mail upload recipient address. |
| `reportok` | boolean | Whether success reports are enabled. |
| `reportto` | string | Report recipient. |
| `status` | string | Mail upload status. |
| `subfolder` | boolean | Whether uploads land in a subfolder. |
| `ttl` | number | Time-to-live in seconds. |

## Native endpoint

Through the native HiDrive API, this operation is `GET /mailupload` (base URL `https://api.hidrive.strato.com/2.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-mail-uploads.md) for the provider-specific parameters and requirements.

