# SelectPdf Universal API Examples

These examples use the MindCloud API key and SelectPdf connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get API Usage



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/selectPdf/latest/actions/get-api-usage?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/selectPdf/latest/actions/get-api-usage?${params}`, {
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
      "available": 1,
      "history": [
        {}
      ],
      "limit": 1,
      "status": "string",
      "subscriptionType": "string",
      "used": 1
    }
  ],
  "meta": {}
}
```

See the full [Get API Usage action reference](actions/get-api-usage.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/selectPdf/latest/actions/get-api-usage).

## Convert HTML to PDF



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/selectPdf/latest/actions/convert-html-to-pdf" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "html": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/selectPdf/latest/actions/convert-html-to-pdf', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "html": "string"
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
      "data": [
        1
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Convert HTML to PDF action reference](actions/convert-html-to-pdf.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/selectPdf/latest/actions/convert-html-to-pdf).
