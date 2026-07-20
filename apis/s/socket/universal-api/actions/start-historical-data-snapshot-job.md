# Socket: Start Historical Data Snapshot Job

Starts a historical data snapshot job in Socket.

```
POST https://connect.mindcloud.co/v1/universal/socket/latest/actions/start-historical-data-snapshot-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Socket `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/socket/latest/actions/start-historical-data-snapshot-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/socket/latest/actions/start-historical-data-snapshot-job', {
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



## Response

```json
{
  "success": true,
  "data": [
    {
      "requestedAt": "string",
      "requestedBy": "string",
      "requestId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `requestedAt` | string |  |
| `requestedBy` | string |  |
| `requestId` | string |  |

## Native endpoint

Through the native Socket API, this operation is `POST /orgs/:org_slug/historical/snapshots` (base URL `https://api.socket.dev/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/start-historical-data-snapshot-job.md) for the provider-specific parameters and requirements.

