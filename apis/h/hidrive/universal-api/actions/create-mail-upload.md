# HiDrive: Create Mail Upload

Creates a new mail upload in HiDrive.

```
POST https://connect.mindcloud.co/v1/universal/hidrive/latest/actions/create-mail-upload
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HiDrive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hidrive/latest/actions/create-mail-upload" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hidrive/latest/actions/create-mail-upload', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `path` | string | no | Directory path for the mail upload. |
| `pid` | string | no | Directory public ID for the mail upload. |
| `rcptSecret` | string | no | Secret component for the mail upload address. |
| `rcptString` | string | no | Local part of the generated mail upload address. |
| `unique` | string | no | Unique identifier returned by Get Unique Identifier. |
| `uniqueMac` | string | no | MAC returned with the unique identifier. |
| `ttl` | number | no | Mail upload expiry in seconds. |
| `overwrite` | boolean | no | Allow uploaded files to overwrite existing files. Default: `false`. |
| `reportok` | boolean | no | Send success notification report. Default: `false`. |

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

Through the native HiDrive API, this operation is `POST /mailupload` (base URL `https://api.hidrive.strato.com/2.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-mail-upload.md) for the provider-specific parameters and requirements.

