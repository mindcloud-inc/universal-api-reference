# Doppler Farhan Latif Universal API Examples

These examples use the MindCloud API key and Doppler Farhan Latif connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Projects

Retrieves projects from Doppler.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dopplerFarhanLatif/latest/actions/list-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dopplerFarhanLatif/latest/actions/list-projects?${params}`, {
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": "string",
      "name": "Ava Chen",
      "slug": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Projects action reference](actions/list-projects.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dopplerFarhanLatif/latest/actions/list-projects).

## Update Secret Note

Updates a secret note in Doppler.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/dopplerFarhanLatif/latest/actions/update-secret-note" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "project": "string",
  "secret": "string",
  "note": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dopplerFarhanLatif/latest/actions/update-secret-note', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "project": "string",
    "secret": "string",
    "note": "string"
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
      "note": "string",
      "secret": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Update Secret Note action reference](actions/update-secret-note.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dopplerFarhanLatif/latest/actions/update-secret-note).
