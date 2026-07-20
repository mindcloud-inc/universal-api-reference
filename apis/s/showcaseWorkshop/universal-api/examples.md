# Showcase Workshop Universal API Examples

These examples use the MindCloud API key and Showcase Workshop connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Data

Retrieves data items from Showcase Workshop.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/showcaseWorkshop/latest/actions/list-data?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/showcaseWorkshop/latest/actions/list-data?${params}`, {
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
      "content": "string",
      "dataName": "Ava Chen",
      "dataType": "string",
      "dateInserted": "2026-05-07T12:00:00.000Z",
      "dateUpdated": "2026-05-07T12:00:00.000Z",
      "guid": "string",
      "showcaseId": 1,
      "showcaseName": "Ava Chen",
      "userEmail": "ava@example.com",
      "userFirstName": "Ava",
      "userId": 1,
      "userLastName": "Chen"
    }
  ],
  "meta": {}
}
```

See the full [List Data action reference](actions/list-data.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/showcaseWorkshop/latest/actions/list-data).

## Add Data

Creates a data item in Showcase Workshop.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/showcaseWorkshop/latest/actions/add-data" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "dataName": "Form1",
  "showcaseId": 1,
  "userEmail": "name@example.com",
  "content": "[object Object]",
  "dateEntered": "2013-01-28T13:01:01Z"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/showcaseWorkshop/latest/actions/add-data', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "dataName": "Form1",
    "showcaseId": 1,
    "userEmail": "name@example.com",
    "content": "[object Object]",
    "dateEntered": "2013-01-28T13:01:01Z"
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
      "content": "string",
      "dataName": "Ava Chen",
      "dataType": "string",
      "dateInserted": "2026-05-07T12:00:00.000Z",
      "guid": "string",
      "showcaseId": 1,
      "showcaseName": "Ava Chen",
      "userEmail": "ava@example.com"
    }
  ],
  "meta": {}
}
```

See the full [Add Data action reference](actions/add-data.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/showcaseWorkshop/latest/actions/add-data).
