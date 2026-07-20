# Monta: Get Charge KWh Consumption

Retrieves charge consumption breakdowns from Monta.

```
GET https://connect.mindcloud.co/v1/universal/monta/latest/actions/get-charge-kwh-consumption
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Monta `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/monta/latest/actions/get-charge-kwh-consumption?connectionId=$CONNECTION_ID&chargeId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "chargeId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/monta/latest/actions/get-charge-kwh-consumption?${params}`, {
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
| `chargeId` | number | yes | ID of the charge to retrieve kWh consumption for. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `consumptionPeriodSizeInSeconds` | list<number> | no | Consumption interval size in seconds. Supported values are 3600, 1800, 900, 600, and 300. One of: `1800`, `300`, `3600`, `600`, `900`. Default: `3600`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "chargeId": 1,
      "consumptionPeriodSizeInSeconds": 1,
      "kwhConsumption": [
        {
          "time": "2026-05-07T12:00:00.000Z",
          "value": 1
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `chargeId` | number |  |
| `consumptionPeriodSizeInSeconds` | number |  |
| `kwhConsumption[].time` | date |  |
| `kwhConsumption[].value` | number |  |

## Native endpoint

Through the native Monta API, this operation is `GET /charges/{chargeId}/kwh-consumption` (base URL `https://public-api.monta.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-charge-kwh-consumption.md) for the provider-specific parameters and requirements.

