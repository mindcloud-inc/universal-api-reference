# Coast Universal API Examples

These examples use the MindCloud API key and Coast connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get My Account



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coast/latest/actions/getmyaccount?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coast/latest/actions/getmyaccount?${params}`, {
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
      "address": {},
      "companyEmail": "ava@example.com",
      "id": "string",
      "legalName": "Ava Chen",
      "name": "Ava Chen",
      "settings": {},
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get My Account action reference](actions/getmyaccount.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/coast/latest/actions/getmyaccount).

## Create Department



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/coast/latest/actions/createdepartment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/coast/latest/actions/createdepartment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
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

See the full [Create Department action reference](actions/createdepartment.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/coast/latest/actions/createdepartment).
