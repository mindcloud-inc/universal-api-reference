# PDF Snake Universal API Examples

These examples use the MindCloud API key and PDF Snake connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Byte Balance

Retrieves your current byte balance from PDF Snake.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pDFSnake/latest/actions/get-byte-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pDFSnake/latest/actions/get-byte-balance?${params}`, {
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
      "balance": 1
    }
  ],
  "meta": {}
}
```

See the full [Get Byte Balance action reference](actions/get-byte-balance.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pDFSnake/latest/actions/get-byte-balance).

## Impose Document

Creates an imposed document from uploaded files in PDF Snake.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pDFSnake/latest/actions/impose-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "doc": "https://pdfsnake.com/pdf/in.pdf",
  "steps": "W10="
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pDFSnake/latest/actions/impose-document', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "doc": "https://pdfsnake.com/pdf/in.pdf",
    "steps": "W10="
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

See the full [Impose Document action reference](actions/impose-document.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pDFSnake/latest/actions/impose-document).
