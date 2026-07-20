# Dext Universal API Examples

These examples use the MindCloud API key and Dext connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Clients

Retrieves all accessible clients from Dext.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dext/latest/actions/list-clients?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dext/latest/actions/list-clients?${params}`, {
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
      "alertLevel": "string",
      "healthScore": 1,
      "id": "string",
      "name": "Ava Chen",
      "practiceCode": "string",
      "providerName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [List Clients action reference](actions/list-clients.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dext/latest/actions/list-clients).
