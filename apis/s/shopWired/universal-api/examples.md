# ShopWired Universal API Examples

These examples use the MindCloud API key and ShopWired connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Retrieve business details

Retrieves business details from ShopWired.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shopWired/latest/actions/get-business?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shopWired/latest/actions/get-business?${params}`, {
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
      "active": true,
      "countryCode": "string",
      "currency": "string",
      "domain": "string",
      "id": 1,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Retrieve business details action reference](actions/get-business.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/shopWired/latest/actions/get-business).
