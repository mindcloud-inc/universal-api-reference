# Clio Manage Universal API Examples

These examples use the MindCloud API key and Clio Manage connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Contacts

Retrieves contacts from your Clio Manage account.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clio/latest/actions/list-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clio/latest/actions/list-contacts?${params}`, {
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
      "etag": "string",
      "id": 1,
      "initials": "string",
      "name": "Ava Chen",
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Contacts action reference](actions/list-contacts.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/clio/latest/actions/list-contacts).

## Create Activity Description

Creates a new activity description in Clio Manage.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/clio/latest/actions/create-activity-description" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "data.name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clio/latest/actions/create-activity-description', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "data.name": "Ava Chen"
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
      "etag": "string",
      "id": 1,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Create Activity Description action reference](actions/create-activity-description.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/clio/latest/actions/create-activity-description).
