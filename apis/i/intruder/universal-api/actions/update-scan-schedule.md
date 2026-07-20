# Intruder: Update Scan Schedule



```
PUT https://connect.mindcloud.co/v1/universal/intruder/latest/actions/update-scan-schedule
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Intruder `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/intruder/latest/actions/update-scan-schedule" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/intruder/latest/actions/update-scan-schedule', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Scan schedule ID. |
| `name` | string | no | Schedule name. |
| `firstScanTime` | date | no | First scan time in the future on the hour. |
| `scanFrequency` | string | no | How often the schedule runs. |
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
      "notice": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `notice` | string |  |

## Native endpoint

Through the native Intruder API, this operation is `PATCH /scans/schedules/:id/` (base URL `https://api.intruder.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-scan-schedule.md) for the provider-specific parameters and requirements.

