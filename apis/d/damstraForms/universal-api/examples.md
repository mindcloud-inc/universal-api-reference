# Damstra Forms Universal API Examples

These examples use the MindCloud API key and Damstra Forms connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Projects

Retrieves projects from Damstra Forms.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/damstraForms/latest/actions/list-projects?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/damstraForms/latest/actions/list-projects?${params}`, {
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
      "active": true,
      "address": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "href": "string",
      "id": 1,
      "inheritWbsItems": true,
      "jobNumber": "string",
      "lockVersion": 1,
      "managed": true,
      "name": "Ava Chen",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "userId": 1,
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Projects action reference](actions/list-projects.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/damstraForms/latest/actions/list-projects).

## Close Form

Closes a form in Damstra Forms.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/damstraForms/latest/actions/close-form" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "submitterUserId": "string",
  "lockVersion": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/damstraForms/latest/actions/close-form', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "submitterUserId": "string",
    "lockVersion": 1
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
      "href": "string"
    }
  ],
  "meta": {}
}
```

See the full [Close Form action reference](actions/close-form.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/damstraForms/latest/actions/close-form).
