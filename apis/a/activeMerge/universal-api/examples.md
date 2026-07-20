# ActiveMerge Universal API Examples

These examples use the MindCloud API key and ActiveMerge connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get User Credits

Retrieves remaining user credits from ActiveMerge.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/activeMerge/latest/actions/get-user-credits?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/activeMerge/latest/actions/get-user-credits?${params}`, {
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
      "left": 1,
      "total": 1,
      "used": 1
    }
  ],
  "meta": {}
}
```

See the full [Get User Credits action reference](actions/get-user-credits.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/activeMerge/latest/actions/get-user-credits).

## Generate Document

Generates a document from a template in ActiveMerge.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/activeMerge/latest/actions/generate-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "data": "[object Object]",
  "format": "pdf",
  "templateId": "tmpl_123"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/activeMerge/latest/actions/generate-document', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "data": "[object Object]",
    "format": "pdf",
    "templateId": "tmpl_123"
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

See the full [Generate Document action reference](actions/generate-document.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/activeMerge/latest/actions/generate-document).
