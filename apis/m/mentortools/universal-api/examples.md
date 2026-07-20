# Mentortools Universal API Examples

These examples use the MindCloud API key and Mentortools connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Courses

Retrieves a list of courses from Mentortools.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mentortools/latest/actions/list-courses?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mentortools/latest/actions/list-courses?${params}`, {
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
      "done": true,
      "result": [
        {
          "id": 1,
          "isActive": true,
          "order": 1,
          "title": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Courses action reference](actions/list-courses.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/mentortools/latest/actions/list-courses).

## Create Folder

Creates a new folder in Mentortools.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mentortools/latest/actions/create-folder" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mentortools/latest/actions/create-folder', {
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
  "data": [
    {
      "done": true,
      "result": 1
    }
  ],
  "meta": {}
}
```

See the full [Create Folder action reference](actions/create-folder.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/mentortools/latest/actions/create-folder).
