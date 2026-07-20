# HiDrive: Update Mail Upload

Updates an existing mail upload in HiDrive.

```
PUT https://connect.mindcloud.co/v1/universal/hidrive/latest/actions/update-mail-upload
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HiDrive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/hidrive/latest/actions/update-mail-upload" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "path": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hidrive/latest/actions/update-mail-upload', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "path": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `path` | string | yes | Mail upload path to update. |
| `pid` | string | no | Mail upload public ID to update. |

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

Through the native HiDrive API, this operation is `PUT /mailupload` (base URL `https://api.hidrive.strato.com/2.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-mail-upload.md) for the provider-specific parameters and requirements.

