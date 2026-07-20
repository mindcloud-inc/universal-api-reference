# Zoho WorkDrive Universal API Examples

These examples use the MindCloud API key and Zoho WorkDrive connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get User Info

Retrieves current user details from Zoho WorkDrive.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoWorkDrive/latest/actions/get-user-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoWorkDrive/latest/actions/get-user-info?${params}`, {
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
      "attributes": {},
      "id": "string",
      "links": {},
      "relationships": {},
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get User Info action reference](actions/get-user-info.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/zohoWorkDrive/latest/actions/get-user-info).

## Add Label to File/Folder

Adds a label to a Zoho WorkDrive file or folder.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoWorkDrive/latest/actions/add-label-to-file-folder" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "labelId": "string",
  "data[].id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoWorkDrive/latest/actions/add-label-to-file-folder', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "labelId": "string",
    "data[].id": "string"
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

See the full [Add Label to File/Folder action reference](actions/add-label-to-file-folder.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/zohoWorkDrive/latest/actions/add-label-to-file-folder).
