# FDIC Universal API Examples

These examples use the MindCloud API key and FDIC connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Bank Failures

Retrieves failed bank records from FDIC.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fDIC/latest/actions/list-bank-failures?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fDIC/latest/actions/list-bank-failures?${params}`, {
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
      "CERT": 1,
      "CITY": "string",
      "COST": 1,
      "FAILDATE": "string",
      "FAILYR": "string",
      "ID": "string",
      "NAME": "Ava Chen",
      "PSTALP": "string",
      "QBFASSET": 1,
      "QBFDEP": 1,
      "RESTYPE": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Bank Failures action reference](actions/list-bank-failures.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/fDIC/latest/actions/list-bank-failures).
