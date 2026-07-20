# BKK Futar Universal API Examples

These examples use the MindCloud API key and BKK Futar connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Bicycle Rental Stations

Retrieves bicycle rental stations from BKK Futar.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bKKFutar/latest/actions/get-bicycle-rental-stations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bKKFutar/latest/actions/get-bicycle-rental-stations?${params}`, {
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
      "limitExceeded": true,
      "list": {
        "bikes": 1,
        "code": "string",
        "id": "string",
        "lat": 1,
        "lon": 1,
        "name": "Ava Chen",
        "type": "string"
      },
      "references": {}
    }
  ],
  "meta": {}
}
```

See the full [Get Bicycle Rental Stations action reference](actions/get-bicycle-rental-stations.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/bKKFutar/latest/actions/get-bicycle-rental-stations).
