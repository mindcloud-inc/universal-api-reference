# Samsara Universal API Examples

These examples use the MindCloud API key and Samsara connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Organization



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/samsara/latest/actions/get-organization?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/samsara/latest/actions/get-organization?${params}`, {
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
      "carrierSettings": {
        "carrierName": "Ava Chen",
        "dotNumber": 1,
        "mainOfficeAddress": "string"
      },
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Get Organization action reference](actions/get-organization.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/samsara/latest/actions/get-organization).

## Create Driver



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/samsara/latest/actions/create-driver" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/samsara/latest/actions/create-driver', {
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
  "data": [],
  "meta": {}
}
```

See the full [Create Driver action reference](actions/create-driver.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/samsara/latest/actions/create-driver).
