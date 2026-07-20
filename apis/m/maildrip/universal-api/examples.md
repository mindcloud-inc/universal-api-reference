# Maildrip Universal API Examples

These examples use the MindCloud API key and Maildrip connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get user details



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/get-user-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/get-user-details?${params}`, {
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
      "accessLevel": {},
      "emailSettings": {},
      "user": {}
    }
  ],
  "meta": {}
}
```

See the full [Get user details action reference](actions/get-user-details.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/maildrip/latest/actions/get-user-details).

## Add a contact



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/add-a-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/add-a-contact', {
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
      "data": {},
      "message": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add a contact action reference](actions/add-a-contact.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/maildrip/latest/actions/add-a-contact).
