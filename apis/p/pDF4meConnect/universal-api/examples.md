# PDF4me Connect Universal API Examples

These examples use the MindCloud API key and PDF4me Connect connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Validate Credentials



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pDF4meConnect/latest/actions/validate-credentials?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pDF4meConnect/latest/actions/validate-credentials?${params}`, {
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
      "author": "string",
      "creationDate": "2026-05-07T12:00:00.000Z",
      "creator": "string",
      "documentId": "string",
      "isEncrypted": true,
      "isLinearized": true,
      "isSigned": true,
      "keywords": "string",
      "modDate": "2026-05-07T12:00:00.000Z",
      "orientation": "string",
      "pageCount": 1,
      "pageHeightInMM": 1,
      "pageWidthInMM": 1,
      "pdfCompliance": "string",
      "pdfVersion": "string",
      "producer": "string",
      "size": 1,
      "subject": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

See the full [Validate Credentials action reference](actions/validate-credentials.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pDF4meConnect/latest/actions/validate-credentials).
