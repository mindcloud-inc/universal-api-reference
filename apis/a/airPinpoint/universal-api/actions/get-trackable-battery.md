# AirPinpoint: Get Trackable Battery

Retrieves battery status for a trackable in AirPinpoint.

```
GET https://connect.mindcloud.co/v1/universal/airPinpoint/latest/actions/get-trackable-battery
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AirPinpoint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/airPinpoint/latest/actions/get-trackable-battery?connectionId=$CONNECTION_ID&trackableId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "trackableId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/airPinpoint/latest/actions/get-trackable-battery?${params}`, {
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
| `trackableId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "batteryMonths": 1,
      "estimatedDaysRemaining": 1,
      "lastBatteryReset": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `batteryMonths` | number |  |
| `estimatedDaysRemaining` | number |  |
| `lastBatteryReset` | date |  |

## Native endpoint

Through the native AirPinpoint API, this operation is `GET /trackables/{trackableId}/battery` (base URL `https://api.airpinpoint.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-trackable-battery.md) for the provider-specific parameters and requirements.

