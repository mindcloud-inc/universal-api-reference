# GraphHopper Universal API Examples

These examples use the MindCloud API key and GraphHopper connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Geocode Location

Retrieves geocoding results for a query in GraphHopper.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/graphHopper/latest/actions/get-geocode?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/graphHopper/latest/actions/get-geocode?${params}`, {
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
      "hits": [
        {}
      ],
      "locale": "string"
    }
  ],
  "meta": {}
}
```

See the full [Geocode Location action reference](actions/get-geocode.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/graphHopper/latest/actions/get-geocode).

## Create Custom Routing Profile

Creates a custom routing profile in GraphHopper.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/graphHopper/latest/actions/create-custom-routing-profile" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "requestBody": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/graphHopper/latest/actions/create-custom-routing-profile', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "requestBody": {}
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "bounds": {},
      "custom_model": {},
      "id": "string",
      "profile": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Custom Routing Profile action reference](actions/create-custom-routing-profile.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/graphHopper/latest/actions/create-custom-routing-profile).
