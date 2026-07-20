# U-ON Universal API Examples

These examples use the MindCloud API key and U-ON connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Companies

Retrieves company records stored in U-ON.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uON/latest/actions/list-companies?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uON/latest/actions/list-companies?${params}`, {
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
      "address_p": "string",
      "address_u": "string",
      "city": "string",
      "fullname": "Ava Chen",
      "id": 1,
      "inn": "string",
      "kpp": "string",
      "name": "Ava Chen",
      "name_rus": "Ava Chen",
      "phones": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Companies action reference](actions/list-companies.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/uON/latest/actions/list-companies).
