# Intruder: List Scan Schedules



```
GET https://connect.mindcloud.co/v1/universal/intruder/latest/actions/list-scan-schedules
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Intruder `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/intruder/latest/actions/list-scan-schedules?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/intruder/latest/actions/list-scan-schedules?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "firstScanTime": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "lastScanEndTime": "2026-05-07T12:00:00.000Z",
      "lastScanStartTime": "2026-05-07T12:00:00.000Z",
      "latestScanId": 1,
      "latestScanStatus": "string",
      "name": "Ava Chen",
      "nextScanDate": "2026-05-07T12:00:00.000Z",
      "schedulePeriod": "string",
      "status": "string",
      "targets": [
        "string"
      ],
      "targetTags": [
        "string"
      ],
      "throttled": true,
      "uploadToDrata": true,
      "uploadToVanta": true,
      "webPortsOnly": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `firstScanTime` | date | The timestamp of the first scheduled scan. |
| `id` | number | The Intruder scan schedule identifier. |
| `lastScanEndTime` | date | When the most recent scheduled scan ended. |
| `lastScanStartTime` | date | When the most recent scheduled scan started. |
| `latestScanId` | number | The most recent scan identifier for this schedule. |
| `latestScanStatus` | string | The status of the most recent scan for this schedule. |
| `name` | string | The scan schedule name. |
| `nextScanDate` | date | The timestamp of the next scheduled scan. |
| `schedulePeriod` | string | How often the schedule runs. |
| `status` | string | The current schedule status. |
| `targets` | array<string> | Targets included directly in the schedule. |
| `targetTags` | array<string> | Target tags included in the schedule. |
| `throttled` | boolean | Whether scans from this schedule run in throttled mode. |
| `uploadToDrata` | boolean | Whether findings from this schedule are uploaded to Drata. |
| `uploadToVanta` | boolean | Whether findings from this schedule are uploaded to Vanta. |
| `webPortsOnly` | boolean | Whether scans from this schedule are limited to web ports only. |

## Native endpoint

Through the native Intruder API, this operation is `GET /scans/schedules/` (base URL `https://api.intruder.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-scan-schedules.md) for the provider-specific parameters and requirements.

