# Fleetio: Create Meter Entry

Creates a new meter entry in Fleetio.

```
POST https://connect.mindcloud.co/v1/universal/fleetio/latest/actions/create-meter-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fleetio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fleetio/latest/actions/create-meter-entry" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "vehicleId": 1,
  "value": 1,
  "date": "2026-05-07T12:00:00.000Z"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fleetio/latest/actions/create-meter-entry', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "vehicleId": 1,
    "value": 1,
    "date": "2026-05-07T12:00:00.000Z"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `vehicleId` | number | yes |  |
| `value` | number | yes | The value of the meter. The unit can be configured at the `Account` level, or overridden at the `Vehicle` level. |
| `date` | date | yes | Meter Entries must follow the correct sequence, incrementing in value by date. For each entry, Fleetio validates to ensure that the value falls between any entries logged before and/or after. We recommend using [ISO-8601](/docs/overview/date-formatting) formatted dates to avoid ambiguity. |
| `void` | boolean | no | Whether to mark this Meter Entry void or not. See [Voiding Meter Entries](https://help.fleetio.com/s/article/Meter-Entry-Mark-As-Void-Unmark-As-Void). |
| `meterType` | string | no | If this is a secondary meter reading, use this field. If the vehicle's secondary meter is disabled, secondary meter values will be hidden in the web and mobile views until enabled. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": 1,
      "activeMeterConflictsCausedCount": 1,
      "autoVoidedAt": "string",
      "autoVoidReason": "string",
      "category": {},
      "createdAt": "string",
      "date": "string",
      "gpsDeviceId": {},
      "gpsProvider": {},
      "id": 1,
      "isSample": true,
      "meterableId": {},
      "meterableType": {},
      "meterType": {},
      "source": "string",
      "updatedAt": "string",
      "value": "string",
      "vehicleArchivedAt": {},
      "vehicleId": 1,
      "void": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | number |  |
| `activeMeterConflictsCausedCount` | number |  |
| `autoVoidedAt` | string |  |
| `autoVoidReason` | string |  |
| `category` | object |  |
| `createdAt` | string |  |
| `date` | string |  |
| `gpsDeviceId` | object |  |
| `gpsProvider` | object |  |
| `id` | number |  |
| `isSample` | boolean |  |
| `meterableId` | object |  |
| `meterableType` | object |  |
| `meterType` | object |  |
| `source` | string |  |
| `updatedAt` | string |  |
| `value` | string |  |
| `vehicleArchivedAt` | object |  |
| `vehicleId` | number |  |
| `void` | boolean |  |

## Native endpoint

Through the native Fleetio API, this operation is `POST meter_entries` (base URL `https://secure.fleetio.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-meter-entry.md) for the provider-specific parameters and requirements.

