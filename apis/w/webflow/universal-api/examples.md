# Webflow Universal API Examples

These examples use the MindCloud API key and Webflow connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Sites

Retrieves a list of sites from Webflow.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webflow/latest/actions/list-sites?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/webflow/latest/actions/list-sites?${params}`, {
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
      "createdOn": "2026-05-07T12:00:00.000Z",
      "customDomains": [
        {}
      ],
      "dataCollectionEnabled": true,
      "dataCollectionType": "string",
      "displayName": "Ava Chen",
      "id": "string",
      "lastPublished": "2026-05-07T12:00:00.000Z",
      "lastUpdated": "2026-05-07T12:00:00.000Z",
      "locales": {},
      "parentFolderId": "string",
      "previewUrl": "https://example.com",
      "shortName": "Ava Chen",
      "timeZone": "string",
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Sites action reference](actions/list-sites.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/webflow/latest/actions/list-sites).

## Create Collection

Creates a new collection in Webflow.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/webflow/latest/actions/create-collection" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "siteId": "string",
  "displayName": "Ava Chen",
  "singularName": "Ava Chen",
  "slug": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/webflow/latest/actions/create-collection', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "siteId": "string",
    "displayName": "Ava Chen",
    "singularName": "Ava Chen",
    "slug": "string"
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
      "createdOn": "2026-05-07T12:00:00.000Z",
      "displayName": "Ava Chen",
      "fields": [
        {}
      ],
      "id": "string",
      "lastUpdated": "2026-05-07T12:00:00.000Z",
      "singularName": "Ava Chen",
      "slug": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Collection action reference](actions/create-collection.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/webflow/latest/actions/create-collection).
