# Motive: List driver utilization



```
GET https://connect.mindcloud.co/v1/universal/motive/latest/actions/list-driver-utilization
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Motive `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/motive/latest/actions/list-driver-utilization?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/motive/latest/actions/list-driver-utilization?${params}`, {
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
| `driverIds` | list<number> | no | Filter utilization by one or more driver IDs. Accepts multiple values as an array. |
| `startDate` | date | no | Fetch utilization from this date onward. |
| `endDate` | date | no | Fetch utilization through this date. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "driverIdleRollup": {
        "driver": {
          "driverCompanyId": "string",
          "email": {},
          "firstName": "Ava",
          "id": 1,
          "lastName": "Chen",
          "role": "string",
          "status": "string",
          "username": "Ava Chen"
        },
        "drivingFuel": 1,
        "drivingTime": 1,
        "idleFuel": 1,
        "idleTime": 1,
        "utilization": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `driverIdleRollup.driver.driverCompanyId` | string |  |
| `driverIdleRollup.driver.email` | object |  |
| `driverIdleRollup.driver.firstName` | string |  |
| `driverIdleRollup.driver.id` | number |  |
| `driverIdleRollup.driver.lastName` | string |  |
| `driverIdleRollup.driver.role` | string |  |
| `driverIdleRollup.driver.status` | string |  |
| `driverIdleRollup.driver.username` | string |  |
| `driverIdleRollup.drivingFuel` | number |  |
| `driverIdleRollup.drivingTime` | number |  |
| `driverIdleRollup.idleFuel` | number |  |
| `driverIdleRollup.idleTime` | number |  |
| `driverIdleRollup.utilization` | number |  |

## Native endpoint

Through the native Motive API, this operation is `GET /v2/driver_utilization` (base URL `https://api.gomotive.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-driver-utilization.md) for the provider-specific parameters and requirements.

