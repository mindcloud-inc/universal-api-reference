# DNSFilter Universal API Examples

These examples use the MindCloud API key and DNSFilter connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Networks



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dNSFilter/latest/actions/list-networks?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dNSFilter/latest/actions/list-networks?${params}`, {
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
      "attributes": {},
      "id": "string",
      "relationships": {},
      "type": "string",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Networks action reference](actions/list-networks.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dNSFilter/latest/actions/list-networks).
