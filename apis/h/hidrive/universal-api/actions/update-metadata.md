# HiDrive: Update Metadata

Updates file metadata in HiDrive.

```
PUT https://connect.mindcloud.co/v1/universal/hidrive/latest/actions/update-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HiDrive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/hidrive/latest/actions/update-metadata" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "mtime": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hidrive/latest/actions/update-metadata', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "mtime": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `path` | string | no | File or folder path. |
| `pid` | string | no | HiDrive public ID for the object. |
| `mtime` | number | yes | Unix timestamp to set as object modification time. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean | True when HiDrive returns a successful no-content metadata update response. |

## Native endpoint

Through the native HiDrive API, this operation is `PATCH /meta` (base URL `https://api.hidrive.strato.com/2.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-metadata.md) for the provider-specific parameters and requirements.

