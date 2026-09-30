# MS SharePoint: Create Upload Session



```
POST https://connect.mindcloud.co/v1/universal/mSSharePoint/latest/actions/create-upload-session
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MS SharePoint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mSSharePoint/latest/actions/create-upload-session" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "driveId": "string",
  "parentItemId": "string",
  "fileName": "largefile.dat"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mSSharePoint/latest/actions/create-upload-session', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "driveId": "string",
    "parentItemId": "string",
    "fileName": "largefile.dat"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `driveId` | string | yes |  |
| `parentItemId` | string | yes | The destination folder ID. Use root for the drive root folder. |
| `fileName` | string | yes | Example: `largefile.dat`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `item` | object | no |  |
| `item.conflictBehavior` | list<string> | no | One of: `fail`, `rename`, `replace`. |
| `item.name` | string | no | If supplied, must match File Name. |
| `deferCommit` | boolean | no | Requires a separate completion request after all bytes are uploaded when enabled. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native MS SharePoint API returns.

## Native endpoint

Through the native MS SharePoint API, this operation is `POST /v1.0/drives/:driveId/items/:parentItemId:/:fileName:/createUploadSession` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-upload-session.md) for the provider-specific parameters and requirements.

