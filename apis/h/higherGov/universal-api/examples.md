# HigherGov Universal API Examples

These examples use the MindCloud API key and HigherGov connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Agencies

Retrieves agencies from HigherGov.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/higherGov/latest/actions/list-agencies?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/higherGov/latest/actions/list-agencies?${params}`, {
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
      "agency_abbreviation": "string",
      "agency_key": 1,
      "agency_name": "Ava Chen",
      "agency_type": "string",
      "defense_flag": true,
      "path": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Agencies action reference](actions/list-agencies.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/higherGov/latest/actions/list-agencies).
