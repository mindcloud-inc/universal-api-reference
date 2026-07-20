# Alto Universal API Examples

These examples use the MindCloud API key and Alto connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Branches

Retrieves branch records from your Alto account.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/alto/latest/actions/get-branches?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/alto/latest/actions/get-branches?${params}`, {
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
      "branchId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "defaultMarket": "string",
      "modifiedAt": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Branches action reference](actions/get-branches.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/alto/latest/actions/get-branches).
