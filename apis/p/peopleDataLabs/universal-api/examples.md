# People Data Labs Universal API Examples

These examples use the MindCloud API key and People Data Labs connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Clean Location



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/peopleDataLabs/latest/actions/clean-location?connectionId=$CONNECTION_ID&location=san%20francisco%2C%20california%2C%20united%20states" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "location": "san francisco, california, united states"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/peopleDataLabs/latest/actions/clean-location?${params}`, {
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
      "continent": "string",
      "country": "string",
      "geo": "string",
      "locality": "string",
      "metro": "string",
      "name": "Ava Chen",
      "region": "string",
      "status": 1,
      "subregion": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Clean Location action reference](actions/clean-location.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/peopleDataLabs/latest/actions/clean-location).
