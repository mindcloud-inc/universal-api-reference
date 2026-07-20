# Flespi Universal API Examples

These examples use the MindCloud API key and Flespi connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List devices



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/flespi/latest/actions/list-devices?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/flespi/latest/actions/list-devices?${params}`, {
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
      "device_type_id": 1,
      "id": 1,
      "name": "Ava Chen",
      "result": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [List devices action reference](actions/list-devices.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/flespi/latest/actions/list-devices).

## Calculate intervals from AI logs



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/flespi/latest/actions/create-ai-logs-calculate" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/flespi/latest/actions/create-ai-logs-calculate', {
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

Example response:

```json
{
  "success": true,
  "data": [
    {
      "errors": [
        {}
      ],
      "id": 1,
      "name": "Ava Chen",
      "result": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [Calculate intervals from AI logs action reference](actions/create-ai-logs-calculate.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/flespi/latest/actions/create-ai-logs-calculate).
