# Otiom: Create Patient

Creates a new patient in Otiom.

```
POST https://connect.mindcloud.co/v1/universal/otiom/latest/actions/create-patient
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Otiom `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/otiom/latest/actions/create-patient" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/otiom/latest/actions/create-patient', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `firstName` | string | no | Patient first name. |
| `lastName` | string | no | Patient last name. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `level` | number | no | Safety level for the patient. |
| `lowBatteryPowerSaveMode` | boolean | no | Whether Otiom should enter power save mode below 30% battery. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "administrating": true,
      "avatar": "string",
      "exit_alarm": {
        "configurable": true,
        "enabled": true
      },
      "first_name": "Ava",
      "full_name": "Ava Chen",
      "geofence": {
        "id": 1,
        "points": [
          [
            "string"
          ]
        ]
      },
      "id": 1,
      "last_name": "Chen",
      "level": 1,
      "low_battery_power_save_mode": true,
      "otiom_tags": [
        {}
      ],
      "site": 1,
      "tag_alarm_sensitivity": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `administrating` | boolean |  |
| `avatar` | string |  |
| `exit_alarm.configurable` | boolean |  |
| `exit_alarm.enabled` | boolean |  |
| `first_name` | string |  |
| `full_name` | string |  |
| `geofence.id` | number |  |
| `geofence.points` | array<array> |  |
| `id` | number |  |
| `last_name` | string |  |
| `level` | number |  |
| `low_battery_power_save_mode` | boolean |  |
| `otiom_tags` | array<object> |  |
| `site` | number |  |
| `tag_alarm_sensitivity` | number |  |

## Native endpoint

Through the native Otiom API, this operation is `POST /api/patients/` (base URL `https://api.otiom.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-patient.md) for the provider-specific parameters and requirements.

