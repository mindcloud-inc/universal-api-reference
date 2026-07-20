# Timeular Universal API Examples

These examples use the MindCloud API key and Timeular connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Generate Report

Generates a time entry report in your Timeular workspace.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timeular/latest/actions/generate-report?connectionId=$CONNECTION_ID&date=string&fileType=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "date": "string",
  "fileType": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timeular/latest/actions/generate-report?${params}`, {
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
      "timeEntries": [
        {
          "activity": {
            "color": "string",
            "folderId": "string",
            "id": "string",
            "name": "Ava Chen"
          },
          "duration": {
            "startedAt": "string",
            "stoppedAt": "string"
          },
          "folder": {
            "id": "string",
            "name": "Ava Chen"
          },
          "id": "string",
          "note": {
            "mentions": [
              {
                "folderId": "string",
                "id": 1,
                "key": "string",
                "label": "string",
                "scope": "string"
              }
            ],
            "tags": [
              [
                "string"
              ]
            ],
            "text": "string"
          },
          "timezone": "string",
          "user": {
            "email": "ava@example.com",
            "id": "string",
            "name": "Ava Chen"
          }
        }
      ]
    }
  ],
  "meta": {}
}
```

See the full [Generate Report action reference](actions/generate-report.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/timeular/latest/actions/generate-report).

## Add Member to Folder

Adds a member to a folder in your Timeular workspace.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/timeular/latest/actions/add-member-to-folder" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com",
  "folderId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/timeular/latest/actions/add-member-to-folder', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com",
    "folderId": "string"
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
      "accessLevel": "string",
      "email": "ava@example.com",
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Add Member to Folder action reference](actions/add-member-to-folder.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/timeular/latest/actions/add-member-to-folder).
