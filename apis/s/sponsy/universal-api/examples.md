# Sponsy Universal API Examples

These examples use the MindCloud API key and Sponsy connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Publications

Retrieves publications from Sponsy.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sponsy/latest/actions/list-publications?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sponsy/latest/actions/list-publications?${params}`, {
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
      "archivedAt": "2026-05-07T12:00:00.000Z",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "days": [
        "string"
      ],
      "hideBlockedDates": true,
      "id": "string",
      "name": "Ava Chen",
      "order": 1,
      "scheduleFrequency": "string",
      "scheduleFrequencyValue": 1,
      "scheduleReferenceTo": "string",
      "slug": "string",
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [List Publications action reference](actions/list-publications.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sponsy/latest/actions/list-publications).

## Create Customer

Creates a customer in Sponsy.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sponsy/latest/actions/create-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "contact.firstName": "Ava",
  "contact.lastName": "Chen",
  "contact.email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sponsy/latest/actions/create-customer', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "contact.firstName": "Ava",
    "contact.lastName": "Chen",
    "contact.email": "ava@example.com"
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
      "allowPortalReports": true,
      "archivedAt": "2026-05-07T12:00:00.000Z",
      "contacts": [
        {}
      ],
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "includeInMetrics": true,
      "name": "Ava Chen",
      "portalId": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Customer action reference](actions/create-customer.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sponsy/latest/actions/create-customer).
