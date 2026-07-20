# SMSEdge Universal API Examples

These examples use the MindCloud API key and SMSEdge connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get User Details

Retrieves API user details from SMSEdge.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sMSEdge/latest/actions/get-user-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sMSEdge/latest/actions/get-user-details?${params}`, {
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

See the full [Get User Details action reference](actions/get-user-details.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sMSEdge/latest/actions/get-user-details).

## Create Contact

Creates a new contact in a SMSEdge list.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sMSEdge/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "list_id": 1,
  "number": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sMSEdge/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "list_id": 1,
    "number": "string"
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

See the full [Create Contact action reference](actions/create-contact.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sMSEdge/latest/actions/create-contact).
