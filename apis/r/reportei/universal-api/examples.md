# Reportei Universal API Examples

These examples use the MindCloud API key and Reportei connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Company Settings

Retrieves company settings from Reportei.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reportei/latest/actions/get-company-settings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reportei/latest/actions/get-company-settings?${params}`, {
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
      "company": {
        "id": 1,
        "logo": "string",
        "name": "Ava Chen",
        "type": "string"
      }
    }
  ],
  "meta": {}
}
```

See the full [Get Company Settings action reference](actions/get-company-settings.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/reportei/latest/actions/get-company-settings).

## Create Dashboard

Creates a new dashboard in Reportei.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/reportei/latest/actions/create-dashboard" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "string",
  "subtitle": "string",
  "start": "2026-05-07T12:00:00.000Z",
  "end": "2026-05-07T12:00:00.000Z",
  "templateId": 1,
  "integrationIds[]": [
    1
  ],
  "projectId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/reportei/latest/actions/create-dashboard', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "string",
    "subtitle": "string",
    "start": "2026-05-07T12:00:00.000Z",
    "end": "2026-05-07T12:00:00.000Z",
    "templateId": 1,
    "integrationIds[]": [1],
    "projectId": 1
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
      "dashboard": {
        "external_url": "https://example.com",
        "id": 1,
        "internal_url": "https://example.com",
        "subtitle": "string",
        "title": "string"
      }
    }
  ],
  "meta": {}
}
```

See the full [Create Dashboard action reference](actions/create-dashboard.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/reportei/latest/actions/create-dashboard).
