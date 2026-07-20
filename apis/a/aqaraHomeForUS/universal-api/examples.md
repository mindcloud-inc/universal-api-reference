# Aqara Home for US Universal API Examples

These examples use the MindCloud API key and Aqara Home for US connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Positions

Retrieves subordinate positions from Aqara Home for US.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aqaraHomeForUS/latest/actions/list-positions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aqaraHomeForUS/latest/actions/list-positions?${params}`, {
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
  "data": [],
  "meta": {}
}
```

See the full [List Positions action reference](actions/list-positions.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/aqaraHomeForUS/latest/actions/list-positions).

## Control Resource Device

Updates an Aqara device through resource controls.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/aqaraHomeForUS/latest/actions/control-resource-device" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/aqaraHomeForUS/latest/actions/control-resource-device', {
  method: 'PUT',
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

Example response:

```json
{
  "success": true,
  "data": [],
  "meta": {}
}
```

See the full [Control Resource Device action reference](actions/control-resource-device.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/aqaraHomeForUS/latest/actions/control-resource-device).
