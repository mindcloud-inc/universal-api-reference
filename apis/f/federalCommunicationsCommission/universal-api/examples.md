# Federal Communications Commission Universal API Examples

These examples use the MindCloud API key and Federal Communications Commission connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Search Facilities

Retrieves FCC facilities matching a keyword.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/federalCommunicationsCommission/latest/actions/search-facilities?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/federalCommunicationsCommission/latest/actions/search-facilities?${params}`, {
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
      "message": "string",
      "responseTime": 1,
      "results": {},
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Search Facilities action reference](actions/search-facilities.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/federalCommunicationsCommission/latest/actions/search-facilities).

## Create Folder

Creates a new FCC OPIF folder.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/federalCommunicationsCommission/latest/actions/create-folder" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/federalCommunicationsCommission/latest/actions/create-folder', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
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
      "entity_folder_id": "string",
      "entity_id": "string",
      "folder_name": "Ava Chen",
      "folder_path": "string",
      "parent_folder_id": "string",
      "source_service_code": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Folder action reference](actions/create-folder.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/federalCommunicationsCommission/latest/actions/create-folder).
