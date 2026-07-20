# Mendeley Universal API Examples

These examples use the MindCloud API key and Mendeley connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get My Profile



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mendeley/latest/actions/get-my-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mendeley/latest/actions/get-my-profile?${params}`, {
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

See the full [Get My Profile action reference](actions/get-my-profile.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/mendeley/latest/actions/get-my-profile).

## Add Document To Folder



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mendeley/latest/actions/add-document-to-folder" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "folderId": "4e12ce22-eb4f-45f4-836c-37d13e7ec36d",
  "documentId": "ec9b2249-ab38-354b-8828-740d2a192353"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mendeley/latest/actions/add-document-to-folder', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "folderId": "4e12ce22-eb4f-45f4-836c-37d13e7ec36d",
    "documentId": "ec9b2249-ab38-354b-8828-740d2a192353"
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

See the full [Add Document To Folder action reference](actions/add-document-to-folder.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/mendeley/latest/actions/add-document-to-folder).
