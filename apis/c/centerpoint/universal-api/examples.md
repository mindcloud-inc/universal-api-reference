# Centerpoint Universal API Examples

These examples use the MindCloud API key and Centerpoint connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Budget Type



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/get-budget-type?connectionId=$CONNECTION_ID&BUDGET_TYPE_ID=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "BUDGET_TYPE_ID": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/get-budget-type?${params}`, {
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
      "attributes": {
        "code": "string",
        "color": "string",
        "createdAt": "string",
        "deletedAt": {},
        "name": "Ava Chen",
        "updatedAt": "string"
      },
      "id": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Budget Type action reference](actions/get-budget-type.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/centerpoint/latest/actions/get-budget-type).

## Create Company



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/create-company" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "type": "string",
  "salesStatus": "string",
  "timeZone": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/create-company', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "type": "string",
    "salesStatus": "string",
    "timeZone": "string"
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

See the full [Create Company action reference](actions/create-company.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/centerpoint/latest/actions/create-company).
