# Otiom Universal API Examples

These examples use the MindCloud API key and Otiom connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Patients

Retrieves patients from Otiom.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/otiom/latest/actions/list-patients?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/otiom/latest/actions/list-patients?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

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

See the full [List Patients action reference](actions/list-patients.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/otiom/latest/actions/list-patients).

## Create Geofence

Creates a new geofence in Otiom.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/otiom/latest/actions/create-geofence" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "points": "12.5683,55.6761,12.5684,55.6761,12.5683,55.6762"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/otiom/latest/actions/create-geofence', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "points": "12.5683,55.6761,12.5684,55.6761,12.5683,55.6762"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "administrating": true,
      "id": 1,
      "name": "Ava Chen",
      "patient": 1,
      "patients": [
        1
      ],
      "points": [
        [
          "string"
        ]
      ]
    }
  ],
  "meta": {}
}
```

See the full [Create Geofence action reference](actions/create-geofence.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/otiom/latest/actions/create-geofence).
