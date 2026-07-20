# LightwaveRF Power Universal API Examples

These examples use the MindCloud API key and LightwaveRF Power connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Structures

Retrieves structures from LightwaveRF Power.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lightwaveRFPower/latest/actions/list-structures?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lightwaveRFPower/latest/actions/list-structures?${params}`, {
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
      "featureSets": [
        "string"
      ],
      "groupId": "string",
      "name": "Ava Chen",
      "order": [
        "string"
      ],
      "parentGroups": [
        "string"
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Structures action reference](actions/list-structures.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/lightwaveRFPower/latest/actions/list-structures).

## Add Device

Creates a new device in LightwaveRF Power.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/lightwaveRFPower/latest/actions/add-device" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "type": "string",
  "destinationId": "string",
  "productCode": "string",
  "manufacturerCode": "string",
  "parentGroups": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lightwaveRFPower/latest/actions/add-device', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "type": "string",
    "destinationId": "string",
    "productCode": "string",
    "manufacturerCode": "string",
    "parentGroups": "string"
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
      "deviceId": "string",
      "manufacturerCode": "string",
      "name": "Ava Chen",
      "productCode": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Device action reference](actions/add-device.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/lightwaveRFPower/latest/actions/add-device).
