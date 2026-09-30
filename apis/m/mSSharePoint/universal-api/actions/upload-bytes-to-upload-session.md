# MS SharePoint: Upload Bytes to Upload Session



```
PUT https://connect.mindcloud.co/v1/universal/mSSharePoint/latest/actions/upload-bytes-to-upload-session
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MS SharePoint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/mSSharePoint/latest/actions/upload-bytes-to-upload-session" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "uploadUrl": "https://example.com",
  "file": "string",
  "contentRange": "bytes 0-327679/655360"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mSSharePoint/latest/actions/upload-bytes-to-upload-session', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "uploadUrl": "https://example.com",
    "file": "string",
    "contentRange": "bytes 0-327679/655360"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `uploadUrl` | string | yes | The full uploadUrl returned by Create Upload Session. |
| `file` | file | yes | The file or file fragment to upload in this request. |
| `contentRange` | string | yes | The byte range and total file size, such as bytes 0-327679/655360. Example: `bytes 0-327679/655360`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native MS SharePoint API returns.

## Native endpoint

Through the native MS SharePoint API, this operation is `PUT :uploadUrl`. The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-bytes-to-upload-session.md) for the provider-specific parameters and requirements.

