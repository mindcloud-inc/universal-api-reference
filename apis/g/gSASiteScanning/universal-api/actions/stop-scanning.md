# GSA Site Scanning: Stop Scanning

Requests a scan device to stop sending scan data.

```
PUT https://connect.mindcloud.co/v1/universal/gSASiteScanning/latest/actions/stop-scanning
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GSA Site Scanning `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/gSASiteScanning/latest/actions/stop-scanning" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "00000000-0000-0000-0000-000000000000"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gSASiteScanning/latest/actions/stop-scanning', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "connectionId": "00000000-0000-0000-0000-000000000000"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `connectionId` | string | yes | Connection ID created for the device on which scanning should stop. Example: `00000000-0000-0000-0000-000000000000`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native GSA Site Scanning API returns.

## Native endpoint

Through the native GSA Site Scanning API, this operation is `POST /scan/v2/stopscanning` (base URL `https://api.sitaflex.aero`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/stop-scanning.md) for the provider-specific parameters and requirements.

