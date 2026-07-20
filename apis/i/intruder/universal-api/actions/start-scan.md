# Intruder: Start Scan



```
POST https://connect.mindcloud.co/v1/universal/intruder/latest/actions/start-scan
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Intruder `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/intruder/latest/actions/start-scan" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/intruder/latest/actions/start-scan', {
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
| `targetAddresses[]` | array<string> | no | Optional target addresses to scan. Leave empty to scan all targets. |
| `tagNames[]` | array<string> | no | Optional target tag names to scan. |
| `throttled` | boolean | no | Throttle the scan for reduced scan intensity. |
| `webPortsOnly` | boolean | no | Limit the scan to common web ports only. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "completedTime": "2026-05-07T12:00:00.000Z",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "scanType": "string",
      "schedulePeriod": "string",
      "startTime": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "targetAddresses": [
        "string"
      ],
      "throttled": true,
      "webPortsOnly": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `completedTime` | date |  |
| `createdAt` | date |  |
| `id` | number |  |
| `scanType` | string |  |
| `schedulePeriod` | string |  |
| `startTime` | date |  |
| `status` | string |  |
| `targetAddresses` | array<string> |  |
| `throttled` | boolean |  |
| `webPortsOnly` | boolean |  |

## Native endpoint

Through the native Intruder API, this operation is `POST /scans/` (base URL `https://api.intruder.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/start-scan.md) for the provider-specific parameters and requirements.

