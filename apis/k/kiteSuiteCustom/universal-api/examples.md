# Kite Suite Universal API Examples

These examples use the MindCloud API key and Kite Suite connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Teams



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/list-teams?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/list-teams?${params}`, {
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
      "_id": "string",
      "createdAt": "string",
      "createdBy": "string",
      "description": "string",
      "isTrashed": true,
      "members": [
        "string"
      ],
      "name": "Ava Chen",
      "updatedAt": "string",
      "workspace": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Teams action reference](actions/list-teams.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/kiteSuiteCustom/latest/actions/list-teams).

## API to create a new Gantt entry



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/a-pi-to-create-a-new-gantt-entry" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "body": {},
  "title": "string",
  "projectID": "string",
  "createdBy": "string",
  "isEnable": true,
  "view": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/a-pi-to-create-a-new-gantt-entry', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "body": {},
    "title": "string",
    "projectID": "string",
    "createdBy": "string",
    "isEnable": true,
    "view": "string"
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

See the full [API to create a new Gantt entry action reference](actions/a-pi-to-create-a-new-gantt-entry.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/kiteSuiteCustom/latest/actions/a-pi-to-create-a-new-gantt-entry).
