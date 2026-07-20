# Hiboutik Universal API Examples

These examples use the MindCloud API key and Hiboutik connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Brands

Retrieves product brands from Hiboutik.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hiboutik/latest/actions/list-brands?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hiboutik/latest/actions/list-brands?${params}`, {
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
      "brandEnabled": 1,
      "brandId": 1,
      "brandName": "Ava Chen",
      "brandPosition": 1
    }
  ],
  "meta": {}
}
```

See the full [List Brands action reference](actions/list-brands.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/hiboutik/latest/actions/list-brands).
