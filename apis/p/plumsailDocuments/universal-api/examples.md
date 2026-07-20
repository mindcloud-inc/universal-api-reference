# Plumsail Documents Universal API Examples

These examples use the MindCloud API key and Plumsail Documents connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Profile Info

Retrieves profile information from Plumsail Documents.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/plumsailDocuments/latest/actions/get-profile-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/plumsailDocuments/latest/actions/get-profile-info?${params}`, {
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
      "email": "ava@example.com",
      "licenseInfo": {},
      "licenseStatus": "string",
      "name": "Ava Chen",
      "shortUserId": "string",
      "teamName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Get Profile Info action reference](actions/get-profile-info.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/plumsailDocuments/latest/actions/get-profile-info).

## Add Watermark to PDF

Adds a watermark to a PDF in Plumsail Documents.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/plumsailDocuments/latest/actions/add-watermark-to-pdf" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/plumsailDocuments/latest/actions/add-watermark-to-pdf', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
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
      "link": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Add Watermark to PDF action reference](actions/add-watermark-to-pdf.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/plumsailDocuments/latest/actions/add-watermark-to-pdf).
