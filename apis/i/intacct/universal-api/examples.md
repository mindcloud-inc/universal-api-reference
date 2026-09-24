# Sage Intacct Universal API Examples

These examples use the MindCloud API key and Sage Intacct connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Check GLBATCH Duplicate



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/intacct/latest/actions/check-glbatch-duplicate?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/intacct/latest/actions/check-glbatch-duplicate?${params}`, {
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

See the full [Check GLBATCH Duplicate action reference](actions/check-glbatch-duplicate.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/intacct/latest/actions/check-glbatch-duplicate).

## Create Attachment

Create a supporting document in a Sage Intacct attachment folder, with optional files encoded as base64.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/intacct/latest/actions/create-attachment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "attachments[].attachmentdata": "string",
  "attachments[].attachmenttype": "string",
  "supdocname": "Ava Chen",
  "attachments[].attachmentname": "Ava Chen",
  "supdocfoldername": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/intacct/latest/actions/create-attachment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "attachments[].attachmentdata": "string",
    "attachments[].attachmenttype": "string",
    "supdocname": "Ava Chen",
    "attachments[].attachmentname": "Ava Chen",
    "supdocfoldername": "Ava Chen"
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

See the full [Create Attachment action reference](actions/create-attachment.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/intacct/latest/actions/create-attachment).
