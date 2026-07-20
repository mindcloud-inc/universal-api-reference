# Hipsy Universal API Examples

These examples use the MindCloud API key and Hipsy connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Organisations

Retrieves organisations from Hipsy.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hipsy/latest/actions/list-organisations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hipsy/latest/actions/list-organisations?${params}`, {
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
      "id": 1,
      "logo": "string",
      "name": "Ava Chen",
      "slug": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Organisations action reference](actions/list-organisations.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/hipsy/latest/actions/list-organisations).
