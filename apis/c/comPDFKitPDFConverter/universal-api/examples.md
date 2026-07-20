# ComPDFKit PDF Converter Universal API Examples

These examples use the MindCloud API key and ComPDFKit PDF Converter connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Asset Details

Retrieves processed asset details from ComPDFKit PDF Converter.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/comPDFKitPDFConverter/latest/actions/get-asset-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/comPDFKitPDFConverter/latest/actions/get-asset-details?${params}`, {
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

See the full [Get Asset Details action reference](actions/get-asset-details.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/comPDFKitPDFConverter/latest/actions/get-asset-details).

## Dewarp Document

Creates a dewarped document from an uploaded file.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/comPDFKitPDFConverter/latest/actions/dewarp-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/comPDFKitPDFConverter/latest/actions/dewarp-document', {
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

See the full [Dewarp Document action reference](actions/dewarp-document.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/comPDFKitPDFConverter/latest/actions/dewarp-document).
