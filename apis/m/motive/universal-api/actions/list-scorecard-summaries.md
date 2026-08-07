# Motive: List scorecard summaries



```
GET https://connect.mindcloud.co/v1/universal/motive/latest/actions/list-scorecard-summaries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Motive `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/motive/latest/actions/list-scorecard-summaries?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/motive/latest/actions/list-scorecard-summaries?${params}`, {
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
| `driverIds` | list<number> | no | Filter scorecard summaries by one or more driver IDs. Accepts multiple values as an array. |
| `startDate` | date | no | Calculate scores from this date onward. |
| `endDate` | date | no | Calculate scores through this date. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "driverPerformanceRollup": {
        "driver": {
          "driverCompanyId": "string",
          "firstName": "Ava",
          "id": 1,
          "lastName": "Chen",
          "role": "string",
          "status": "string",
          "username": "Ava Chen"
        },
        "numCoachedEvents": 1,
        "numHardAccels": 1,
        "numHardBrakes": 1,
        "numHardCorners": 1,
        "score": 1,
        "totalKilometers": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `driverPerformanceRollup.driver.driverCompanyId` | string |  |
| `driverPerformanceRollup.driver.firstName` | string |  |
| `driverPerformanceRollup.driver.id` | number |  |
| `driverPerformanceRollup.driver.lastName` | string |  |
| `driverPerformanceRollup.driver.role` | string |  |
| `driverPerformanceRollup.driver.status` | string |  |
| `driverPerformanceRollup.driver.username` | string |  |
| `driverPerformanceRollup.numCoachedEvents` | number |  |
| `driverPerformanceRollup.numHardAccels` | number |  |
| `driverPerformanceRollup.numHardBrakes` | number |  |
| `driverPerformanceRollup.numHardCorners` | number |  |
| `driverPerformanceRollup.score` | number |  |
| `driverPerformanceRollup.totalKilometers` | number |  |

## Native endpoint

Through the native Motive API, this operation is `GET /v1/scorecard_summary` (base URL `https://api.gomotive.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-scorecard-summaries.md) for the provider-specific parameters and requirements.

