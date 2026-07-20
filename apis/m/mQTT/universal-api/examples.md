# MQTT Universal API Examples

These examples use the MindCloud API key and MQTT connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List MQTT Roles

Retrieves MQTT roles from HiveMQ Cloud.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mQTT/latest/actions/list-mqtt-roles?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mQTT/latest/actions/list-mqtt-roles?${params}`, {
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
      "roles": [
        {
          "roleInfo": {
            "description": "string",
            "id": "string",
            "name": "Ava Chen"
          }
        }
      ]
    }
  ],
  "meta": {}
}
```

See the full [List MQTT Roles action reference](actions/list-mqtt-roles.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/mQTT/latest/actions/list-mqtt-roles).

## Attach Permission To Role

Updates an MQTT role in HiveMQ Cloud by attaching a permission.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/mQTT/latest/actions/attach-permission-to-role" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "permissionId": 1,
  "roleId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mQTT/latest/actions/attach-permission-to-role', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "permissionId": 1,
    "roleId": 1
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [],
  "meta": {}
}
```

See the full [Attach Permission To Role action reference](actions/attach-permission-to-role.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/mQTT/latest/actions/attach-permission-to-role).
