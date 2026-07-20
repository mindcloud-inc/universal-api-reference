# Aqara Home for KR Universal API Examples

These examples use the MindCloud API key and Aqara Home for KR connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Devices

Retrieves devices from Aqara Home for KR.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aqaraHomeForKR/latest/actions/list-devices?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aqaraHomeForKR/latest/actions/list-devices?${params}`, {
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
      "createTime": 1,
      "deviceName": "Ava Chen",
      "did": "string",
      "firmwareVersion": "string",
      "model": "string",
      "modelType": 1,
      "parentDid": "string",
      "positionId": "string",
      "state": 1,
      "success": true,
      "timeZone": "string",
      "totalCount": 1,
      "updateTime": 1
    }
  ],
  "meta": {}
}
```

See the full [List Devices action reference](actions/list-devices.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/aqaraHomeForKR/latest/actions/list-devices).

## Create Position

Creates a new position in Aqara Home for KR.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/aqaraHomeForKR/latest/actions/create-position" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "positionName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/aqaraHomeForKR/latest/actions/create-position', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "positionName": "Ava Chen"
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
      "positionId": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Create Position action reference](actions/create-position.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/aqaraHomeForKR/latest/actions/create-position).
