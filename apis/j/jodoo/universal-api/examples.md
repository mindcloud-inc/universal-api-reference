# Jodoo Universal API Examples

These examples use the MindCloud API key and Jodoo connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Apps



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jodoo/latest/actions/list-apps?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jodoo/latest/actions/list-apps?${params}`, {
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
      "appId": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [List Apps action reference](actions/list-apps.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/jodoo/latest/actions/list-apps).

## Create Member



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/jodoo/latest/actions/create-member" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "username": "jodoo_member_001",
  "name": "Wizard Sandbox",
  "departments[]": "1"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/jodoo/latest/actions/create-member', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "username": "jodoo_member_001",
    "name": "Wizard Sandbox",
    "departments[]": "1"
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
      "departments": [
        1
      ],
      "name": "Ava Chen",
      "status": 1,
      "type": 1,
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Create Member action reference](actions/create-member.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/jodoo/latest/actions/create-member).
