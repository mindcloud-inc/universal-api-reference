# PDF-API.io Universal API Examples

These examples use the MindCloud API key and PDF-API.io connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Templates

Retrieves a list of templates from PDF-API.io.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pDFAPIio/latest/actions/list-templates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pDFAPIio/latest/actions/list-templates?${params}`, {
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "meta": {},
      "name": "Ava Chen",
      "teamId": 1,
      "teamName": "Ava Chen",
      "type": "string",
      "variables": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Templates action reference](actions/list-templates.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pDFAPIio/latest/actions/list-templates).

## Merge Templates

Creates one PDF document from multiple templates in PDF-API.io.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pDFAPIio/latest/actions/merge-templates" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "templates[]": [
    {}
  ],
  "templates[].id": 1,
  "templates[].data": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pDFAPIio/latest/actions/merge-templates', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "templates[]": [{}],
    "templates[].id": 1,
    "templates[].data": {}
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
      "status": 1,
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Merge Templates action reference](actions/merge-templates.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pDFAPIio/latest/actions/merge-templates).
