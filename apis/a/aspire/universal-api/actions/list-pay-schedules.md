# Aspire: List Pay Schedules

Retrieves takeoff groups from your Aspire account.

```
GET https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-pay-schedules
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aspire `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-pay-schedules?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-pay-schedules?${params}`, {
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
| `expand` | string | no |  |
| `filter` | string | no |  |
| `orderBy` | string | no |  |
| `select` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "dailyHoursBeforeOT": 1,
      "defaultOTPayCodeID": 1,
      "defaultOTPayCodeName": "Ava Chen",
      "defaultPayCodeID": 1,
      "defaultPayCodeName": "Ava Chen",
      "payScheduleID": 1,
      "payScheduleName": "Ava Chen",
      "weeklyHoursBeforeOT": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `dailyHoursBeforeOT` | number |  |
| `defaultOTPayCodeID` | number |  |
| `defaultOTPayCodeName` | string |  |
| `defaultPayCodeID` | number |  |
| `defaultPayCodeName` | string |  |
| `payScheduleID` | number |  |
| `payScheduleName` | string |  |
| `weeklyHoursBeforeOT` | number |  |

## Native endpoint

Through the native Aspire API, this operation is `GET PaySchedules` (base URL `https://{{credentials.environment}}.youraspire.com/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-pay-schedules.md) for the provider-specific parameters and requirements.

