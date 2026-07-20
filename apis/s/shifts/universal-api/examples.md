# 7shifts Universal API Examples

These examples use the MindCloud API key and 7shifts connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get User Contacts

Lists the user contacts in 7shifts.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shifts/latest/actions/get-user-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shifts/latest/actions/get-user-contacts?${params}`, {
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
      "email": "ava@example.com",
      "first_name": "Ava",
      "id": 1,
      "last_name": "Chen"
    }
  ],
  "meta": {}
}
```

See the full [Get User Contacts action reference](actions/get-user-contacts.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/shifts/latest/actions/get-user-contacts).

## Create Department

Creates a new department in 7shifts.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/shifts/latest/actions/create-department" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/shifts/latest/actions/create-department', {
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
      "id": 1,
      "location_id": 1,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Create Department action reference](actions/create-department.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/shifts/latest/actions/create-department).
