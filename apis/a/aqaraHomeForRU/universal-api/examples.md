# Aqara Home for RU Universal API Examples

These examples use the MindCloud API key and Aqara Home for RU connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Query Position Info

Retrieves child positions from Aqara Home for RU.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aqaraHomeForRU/latest/actions/query-position-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aqaraHomeForRU/latest/actions/query-position-info?${params}`, {
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

See the full [Query Position Info action reference](actions/query-position-info.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/aqaraHomeForRU/latest/actions/query-position-info).

## Update Device Name

Updates a device name in Aqara Home for RU.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/aqaraHomeForRU/latest/actions/config-device-name" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/aqaraHomeForRU/latest/actions/config-device-name', {
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

See the full [Update Device Name action reference](actions/config-device-name.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/aqaraHomeForRU/latest/actions/config-device-name).
