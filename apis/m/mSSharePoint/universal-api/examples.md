# MS SharePoint Universal API Examples

These examples use the MindCloud API key and MS SharePoint connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Root Site

Retrieves the root SharePoint site.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mSSharePoint/latest/actions/get-root-site?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mSSharePoint/latest/actions/get-root-site?${params}`, {
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
      "createdDateTime": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "displayName": "Ava Chen",
      "id": "string",
      "lastModifiedDateTime": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "root": {},
      "sharepointIds": {},
      "siteCollection": {},
      "webUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Get Root Site action reference](actions/get-root-site.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/mSSharePoint/latest/actions/get-root-site).

## Create Folder

Creates a new folder in SharePoint.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mSSharePoint/latest/actions/create-folder" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "driveId": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mSSharePoint/latest/actions/create-folder', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "driveId": "string",
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
      "createdBy": {},
      "createdDateTime": "2026-05-07T12:00:00.000Z",
      "file": {},
      "folder": {},
      "id": "string",
      "lastModifiedBy": {},
      "lastModifiedDateTime": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "parentReference": {},
      "size": 1,
      "webUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Create Folder action reference](actions/create-folder.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/mSSharePoint/latest/actions/create-folder).
