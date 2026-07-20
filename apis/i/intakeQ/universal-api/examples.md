# IntakeQ Universal API Examples

These examples use the MindCloud API key and IntakeQ connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Download File

Retrieves a file from IntakeQ.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/intakeQ/latest/actions/download-file?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/intakeQ/latest/actions/download-file?${params}`, {
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
      "contentType": "string",
      "data": "string",
      "fileName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Download File action reference](actions/download-file.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/intakeQ/latest/actions/download-file).

## Add Client Tag

Creates a client tag assignment in IntakeQ.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/intakeQ/latest/actions/add-client-tag" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "clientId": "string",
  "tag": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/intakeQ/latest/actions/add-client-tag', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "clientId": "string",
    "tag": "string"
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
      "clientId": 1,
      "tag": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Client Tag action reference](actions/add-client-tag.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/intakeQ/latest/actions/add-client-tag).
