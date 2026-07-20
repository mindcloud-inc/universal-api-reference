# Formitize Universal API Examples

These examples use the MindCloud API key and Formitize connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Tasks

Retrieves tasks from Formitize.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/formitize/latest/actions/list-tasks?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/formitize/latest/actions/list-tasks?${params}`, {
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
      "assignedTo": 1,
      "createdBy": 1,
      "dateCreated": 1,
      "dateModified": 1,
      "description": "string",
      "dueDate": 1,
      "id": 1,
      "status": 1,
      "tags": [
        "string"
      ],
      "taskType": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Tasks action reference](actions/list-tasks.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/formitize/latest/actions/list-tasks).

## Add Client

Creates a new client in Formitize.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/formitize/latest/actions/add-client" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/formitize/latest/actions/add-client', {
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
      "billingName": "Ava Chen",
      "contactIDs": [
        1
      ],
      "id": "string",
      "locationIDs": [
        1
      ],
      "primaryAddress": "string",
      "primaryAddressID": 1,
      "primaryContactID": 1,
      "primaryContactName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Add Client action reference](actions/add-client.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/formitize/latest/actions/add-client).
