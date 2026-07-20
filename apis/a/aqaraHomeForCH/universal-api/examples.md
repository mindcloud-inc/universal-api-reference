# Aqara Home for CH Universal API Examples

These examples use the MindCloud API key and Aqara Home for CH connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Positions

Retrieves subordinate positions from Aqara Home for CH.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aqaraHomeForCH/latest/actions/list-positions?connectionId=$CONNECTION_ID&data=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "data": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aqaraHomeForCH/latest/actions/list-positions?${params}`, {
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
      "createTime": "string",
      "description": "string",
      "parentPositionId": "string",
      "positionId": "string",
      "positionName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [List Positions action reference](actions/list-positions.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/aqaraHomeForCH/latest/actions/list-positions).

## Create Position

Creates a new position in Aqara Home for CH.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/aqaraHomeForCH/latest/actions/create-position" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "data": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/aqaraHomeForCH/latest/actions/create-position', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "data": {}
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
      "positionId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Position action reference](actions/create-position.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/aqaraHomeForCH/latest/actions/create-position).
