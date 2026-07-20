# Rebrickable Universal API Examples

These examples use the MindCloud API key and Rebrickable connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Colors

Retrieves LEGO color records from Rebrickable.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rebrickable/latest/actions/list-colors?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rebrickable/latest/actions/list-colors?${params}`, {
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
      "external_ids": {},
      "id": 1,
      "is_trans": true,
      "name": "Ava Chen",
      "rgb": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Colors action reference](actions/list-colors.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/rebrickable/latest/actions/list-colors).
