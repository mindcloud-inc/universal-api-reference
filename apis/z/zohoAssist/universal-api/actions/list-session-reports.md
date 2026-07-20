# Zoho Assist: List Session Reports

Lists reports for previously conducted Zoho Assist sessions.

```
GET https://connect.mindcloud.co/v1/universal/zohoAssist/latest/actions/list-session-reports
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Assist `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoAssist/latest/actions/list-session-reports?connectionId=$CONNECTION_ID&limit=25&offset=0&type=all&fromDate=1&toDate=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "type": "all",
  "fromDate": "1",
  "toDate": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoAssist/latest/actions/list-session-reports?${params}`, {
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
| `type` | string | yes | Report type: rs, URS, or all. Default: `all`. |
| `fromDate` | number | yes | Report start time in Unix milliseconds. |
| `toDate` | number | yes | Report end time in Unix milliseconds. |
| `email` | string | no | Filter reports to a technician email. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "agentEmail": "ava@example.com",
      "agentIpaddress": "string",
      "agentOs": "string",
      "date": 1,
      "displayName": "Ava Chen",
      "duration": "string",
      "endTime": 1,
      "sessionId": 1,
      "sessionOwnerEmail": "ava@example.com",
      "sessionType": "string",
      "startTime": 1,
      "time": 1,
      "viewerEmail": "ava@example.com",
      "viewerIpaddress": "string",
      "viewerOs": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agentEmail` | string |  |
| `agentIpaddress` | string |  |
| `agentOs` | string |  |
| `date` | number |  |
| `displayName` | string |  |
| `duration` | string |  |
| `endTime` | number |  |
| `sessionId` | number |  |
| `sessionOwnerEmail` | string |  |
| `sessionType` | string |  |
| `startTime` | number |  |
| `time` | number |  |
| `viewerEmail` | string |  |
| `viewerIpaddress` | string |  |
| `viewerOs` | string |  |

## Native endpoint

Through the native Zoho Assist API, this operation is `GET /reports` (base URL `https://assist.zoho.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-session-reports.md) for the provider-specific parameters and requirements.

