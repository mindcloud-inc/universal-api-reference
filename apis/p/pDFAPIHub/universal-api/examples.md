# PDF API Hub Universal API Examples

These examples use the MindCloud API key and PDF API Hub connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Extract Text From URL



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pDFAPIHub/latest/actions/extract-text-from-url?connectionId=$CONNECTION_ID&fileUrl=https%3A%2F%2Fwww.adobe.com%2Fsupport%2Fproducts%2Fenterprise%2Fknowledgecenter%2Fmedia%2Fc4611_sample_explain.pdf" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fileUrl": "https://www.adobe.com/support/products/enterprise/knowledgecenter/media/c4611_sample_explain.pdf"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pDFAPIHub/latest/actions/extract-text-from-url?${params}`, {
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
      "filename": "Ava Chen",
      "metadata": {},
      "pages": 1,
      "source": "string",
      "text": "string"
    }
  ],
  "meta": {}
}
```

See the full [Extract Text From URL action reference](actions/extract-text-from-url.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pDFAPIHub/latest/actions/extract-text-from-url).

## Fill PDF



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pDFAPIHub/latest/actions/fill-pdf" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "templateId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pDFAPIHub/latest/actions/fill-pdf', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "templateId": "string"
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

See the full [Fill PDF action reference](actions/fill-pdf.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pDFAPIHub/latest/actions/fill-pdf).
