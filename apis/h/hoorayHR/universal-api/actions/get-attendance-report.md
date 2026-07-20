# HoorayHR: Get Attendance Report

Retrieves an attendance report from HoorayHR.

```
GET https://connect.mindcloud.co/v1/universal/hoorayHR/latest/actions/get-attendance-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HoorayHR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hoorayHR/latest/actions/get-attendance-report?connectionId=$CONNECTION_ID&startDate=string&endDate=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "startDate": "string",
  "endDate": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hoorayHR/latest/actions/get-attendance-report?${params}`, {
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
| `startDate` | string | yes | The report start date in YYYY-MM-DD format. |
| `endDate` | string | yes | The report end date in YYYY-MM-DD format. It cannot be more than 31 days after the start date. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "balanceHours": 1,
      "leaveHours": 1,
      "scheduledHours": 1,
      "sickLeaveHours": 1,
      "userId": 1,
      "writtenHours": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `balanceHours` | number |  |
| `leaveHours` | number |  |
| `scheduledHours` | number |  |
| `sickLeaveHours` | number |  |
| `userId` | number |  |
| `writtenHours` | number |  |

## Native endpoint

Through the native HoorayHR API, this operation is `GET /attendance-report` (base URL `https://api.hoorayhr.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-attendance-report.md) for the provider-specific parameters and requirements.

