# CSVBox Universal API Examples

These examples use the MindCloud API key and CSVBox connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Verify Connection



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cSVBox/latest/actions/verify-connection?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cSVBox/latest/actions/verify-connection?${params}`, {
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
      "data": {},
      "message": "string"
    }
  ],
  "meta": {}
}
```

See the full [Verify Connection action reference](actions/verify-connection.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/cSVBox/latest/actions/verify-connection).

## Submit File From Public URL



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cSVBox/latest/actions/submit-file-from-public-url" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "publicFileUrl": "https://example.com",
  "sheetLicenseKey": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cSVBox/latest/actions/submit-file-from-public-url', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "publicFileUrl": "https://example.com",
    "sheetLicenseKey": "string"
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
      "custom_fields": {},
      "destination_type": "string",
      "dynamic_columns": {},
      "env_name": "Ava Chen",
      "import_id": 1,
      "import_starttime": 1,
      "options": {},
      "sheet_id": 1,
      "sheet_name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Submit File From Public URL action reference](actions/submit-file-from-public-url.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/cSVBox/latest/actions/submit-file-from-public-url).
