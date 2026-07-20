# Connecteam: Get Timesheet Totals

Retrieves detailed work records for each employee within a specified date range. This endpoint is designed to support payroll processing by providing total worked hours, categorized by pay rules and resource (if applied in the account settings). Ideal for integrating with external payroll systems to ensure accurate information. The pay rate will be presented in case it is defined within the account. If an automated unpaid break is applied, it will  be deducted from the total hours value. In order to retrieve approved paid time-off (PTO) and manual break information, please use the Get time activities endpoint. Hours will be presented in decimal format. The time period is limited to 45 days.

```
GET https://connect.mindcloud.co/v1/universal/connecteam/latest/actions/get-timesheet-totals
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Connecteam `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/connecteam/latest/actions/get-timesheet-totals?connectionId=$CONNECTION_ID&timeClockId=1&startDate=string&endDate=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "timeClockId": "1",
  "startDate": "string",
  "endDate": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/connecteam/latest/actions/get-timesheet-totals?${params}`, {
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
| `timeClockId` | number | yes |  |
| `startDate` | string | yes |  |
| `endDate` | string | yes |  |
| `userIds` | array<number> | no | Accepts multiple values as an array. |
| `groupIds` | array<string> | no | Accepts multiple values as an array. |
| `jobIds` | array<string> | no | Accepts multiple values as an array. |
| `isApproved` | boolean | no |  |
| `isSubmitted` | boolean | no |  |
| `isLocked` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "endDate": "string",
      "startDate": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `endDate` | string |  |
| `startDate` | string |  |

## Native endpoint

Through the native Connecteam API, this operation is `GET /time-clock/v1/time-clocks/:timeClockId/timesheet` (base URL `https://api.connecteam.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-timesheet-totals.md) for the provider-specific parameters and requirements.

