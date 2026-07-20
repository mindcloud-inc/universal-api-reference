# Productlane Universal API Examples

These examples use the MindCloud API key and Productlane connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Companies

Retrieves companies from your Productlane workspace.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/productlane/latest/actions/list-companies?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/productlane/latest/actions/list-companies?${params}`, {
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
      "autoAdd": {},
      "Count": {
        "contacts": 1
      },
      "createdAt": "string",
      "domains": [
        "string"
      ],
      "externalIds": [
        "string"
      ],
      "hubspotId": {},
      "id": "string",
      "intercomId": {},
      "isDeleted": true,
      "linearCustomerId": {},
      "logoUrl": {},
      "meta": {},
      "name": "Ava Chen",
      "productboardId": {},
      "revenue": {},
      "size": {},
      "slugId": {},
      "statusColor": {},
      "statusId": {},
      "statusName": {},
      "tierId": {},
      "tierName": {},
      "updatedAt": "string",
      "version": 1,
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Companies action reference](actions/list-companies.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/productlane/latest/actions/list-companies).

## Create Changelog

Creates a new changelog in Productlane.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/productlane/latest/actions/create-changelog" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "string",
  "content": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/productlane/latest/actions/create-changelog', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "string",
    "content": "string"
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
      "archived": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "date": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "imageUrl": "https://example.com",
      "isDeleted": true,
      "notes": {},
      "projectId": "string",
      "published": true,
      "tags": [
        {}
      ],
      "title": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "version": 1,
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Changelog action reference](actions/create-changelog.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/productlane/latest/actions/create-changelog).
