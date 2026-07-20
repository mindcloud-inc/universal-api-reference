# Docupilot Universal API Examples

These examples use the MindCloud API key and Docupilot connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Folders

Retrieves folders from Docupilot.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docupilot/latest/actions/list-folders?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docupilot/latest/actions/list-folders?${params}`, {
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

See the full [List Folders action reference](actions/list-folders.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/docupilot/latest/actions/list-folders).

## Copy Template

Copies a template in Docupilot.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/docupilot/latest/actions/copy-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "folder": 1,
  "title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/docupilot/latest/actions/copy-template', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "folder": 1,
    "title": "string"
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

See the full [Copy Template action reference](actions/copy-template.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/docupilot/latest/actions/copy-template).
