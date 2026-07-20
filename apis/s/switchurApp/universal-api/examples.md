# Switchur App Universal API Examples

These examples use the MindCloud API key and Switchur App connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Switchboard Item Value



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/switchurApp/latest/actions/get-switchboard-item-value?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/switchurApp/latest/actions/get-switchboard-item-value?${params}`, {
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
      "value": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Switchboard Item Value action reference](actions/get-switchboard-item-value.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/switchurApp/latest/actions/get-switchboard-item-value).

## Set Switchboard Item Value



```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/switchurApp/latest/actions/set-switchboard-item-value" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "setToValue": "on"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/switchurApp/latest/actions/set-switchboard-item-value', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "setToValue": "on"
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
      "message": "string"
    }
  ],
  "meta": {}
}
```

See the full [Set Switchboard Item Value action reference](actions/set-switchboard-item-value.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/switchurApp/latest/actions/set-switchboard-item-value).
