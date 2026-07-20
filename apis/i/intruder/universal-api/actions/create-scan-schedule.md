# Intruder: Create Scan Schedule



```
POST https://connect.mindcloud.co/v1/universal/intruder/latest/actions/create-scan-schedule
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Intruder `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/intruder/latest/actions/create-scan-schedule" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "scanFrequency": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/intruder/latest/actions/create-scan-schedule', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "scanFrequency": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Schedule name. |
| `firstScanTime` | date | no | First scan time in the future on the hour. |
| `scanFrequency` | string | yes | How often the schedule runs. |
| `tags[]` | array<string> | no | Tag names to include in the scan. |
| `targets[]` | array<number> | no | Target IDs to include in the scan. |
| `throttled` | boolean | no | Run the schedule in throttled mode. |
| `webPortsOnly` | boolean | no | Limit scans to web ports only. |
| `uploadToDrata` | boolean | no | Upload findings to Drata. |
| `uploadToVanta` | boolean | no | Upload findings to Vanta. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "notice": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `notice` | string |  |

## Native endpoint

Through the native Intruder API, this operation is `POST /scans/schedules/` (base URL `https://api.intruder.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-scan-schedule.md) for the provider-specific parameters and requirements.

