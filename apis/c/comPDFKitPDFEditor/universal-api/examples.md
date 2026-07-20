# ComPDFKit PDF Editor Universal API Examples

These examples use the MindCloud API key and ComPDFKit PDF Editor connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Asset Details

Retrieves remaining asset balances from ComPDFKit PDF Editor.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/comPDFKitPDFEditor/latest/actions/get-asset-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/comPDFKitPDFEditor/latest/actions/get-asset-details?${params}`, {
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
      "code": "string",
      "data": {},
      "msg": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Asset Details action reference](actions/get-asset-details.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/comPDFKitPDFEditor/latest/actions/get-asset-details).

## Add Watermark

Creates a watermarking task in ComPDFKit PDF Editor.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/comPDFKitPDFEditor/latest/actions/add-watermark" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/comPDFKitPDFEditor/latest/actions/add-watermark', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file": "string"
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
      "code": "string",
      "data": {},
      "msg": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Watermark action reference](actions/add-watermark.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/comPDFKitPDFEditor/latest/actions/add-watermark).
