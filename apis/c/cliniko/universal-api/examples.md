# Cliniko Universal API Examples

These examples use the MindCloud API key and Cliniko connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Patients

Retrieves patient records from your Cliniko account.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cliniko/latest/actions/list-patients?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cliniko/latest/actions/list-patients?${params}`, {
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
      "links": {
        "self": "https://example.com"
      },
      "totalEntries": 1
    }
  ],
  "meta": {}
}
```

See the full [List Patients action reference](actions/list-patients.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/cliniko/latest/actions/list-patients).
