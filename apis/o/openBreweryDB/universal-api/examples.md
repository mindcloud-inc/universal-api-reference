# Open Brewery DB Universal API Examples

These examples use the MindCloud API key and Open Brewery DB connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Breweries

Retrieves breweries from Open Brewery DB.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openBreweryDB/latest/actions/list-breweries?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openBreweryDB/latest/actions/list-breweries?${params}`, {
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
      "address_1": "string",
      "address_2": "string",
      "address_3": "string",
      "brewery_type": "string",
      "city": "string",
      "country": "string",
      "id": "string",
      "latitude": 1,
      "longitude": 1,
      "name": "Ava Chen",
      "phone": "string",
      "postal_code": "string",
      "state": "string",
      "state_province": "string",
      "street": "string",
      "website_url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [List Breweries action reference](actions/list-breweries.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/openBreweryDB/latest/actions/list-breweries).
