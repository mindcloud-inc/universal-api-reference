# Vaisala Xweather Universal API Examples

These examples use the MindCloud API key and Vaisala Xweather connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Place

Retrieves place details from Vaisala Xweather API.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vaisalaXweatherAPI/latest/actions/get-place?connectionId=$CONNECTION_ID&id=seattle%2Cwa" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "seattle,wa"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vaisalaXweatherAPI/latest/actions/get-place?${params}`, {
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
      "loc": {},
      "place": {},
      "profile": {}
    }
  ],
  "meta": {}
}
```

See the full [Get Place action reference](actions/get-place.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/vaisalaXweatherAPI/latest/actions/get-place).
