# Intruder: Retrieve Scan Details



```
GET https://connect.mindcloud.co/v1/universal/intruder/latest/actions/retrieve-scan-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Intruder `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/intruder/latest/actions/retrieve-scan-details?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/intruder/latest/actions/retrieve-scan-details?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The Intruder scan identifier. |

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

Through the native Intruder API, this operation is `GET /scans/:id/` (base URL `https://api.intruder.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-scan-details.md) for the provider-specific parameters and requirements.

