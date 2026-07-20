# EARLY Universal API Examples

These examples use the MindCloud API key and EARLY connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Generate Report

Generates a report in EARLY.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eARLY/latest/actions/generate-report?connectionId=$CONNECTION_ID&date.start=string&date.end=string&fileType=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "date.start": "string",
  "date.end": "string",
  "fileType": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eARLY/latest/actions/generate-report?${params}`, {
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

See the full [Generate Report action reference](actions/generate-report.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/eARLY/latest/actions/generate-report).

## Add Member to Folder

Adds a member to an EARLY folder.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/eARLY/latest/actions/add-member-to-folder" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "folderId": "340665",
  "email": "apps@mindcloud.co",
  "accessLevel": "full"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eARLY/latest/actions/add-member-to-folder', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "folderId": "340665",
    "email": "apps@mindcloud.co",
    "accessLevel": "full"
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

See the full [Add Member to Folder action reference](actions/add-member-to-folder.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/eARLY/latest/actions/add-member-to-folder).
