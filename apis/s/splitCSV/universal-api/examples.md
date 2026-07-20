# Split CSV Universal API Examples

These examples use the MindCloud API key and Split CSV connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Retrieve Profile

Retrieves the current user profile from Split CSV.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/splitCSV/latest/actions/retrieve-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/splitCSV/latest/actions/retrieve-profile?${params}`, {
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
      "defaultRetention": 1,
      "email": "ava@example.com",
      "name": "Ava Chen",
      "perFileNotifications": true,
      "provider": "string",
      "timezone": "string"
    }
  ],
  "meta": {}
}
```

See the full [Retrieve Profile action reference](actions/retrieve-profile.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/splitCSV/latest/actions/retrieve-profile).

## Create Order

Creates a new file-processing order in Split CSV.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/splitCSV/latest/actions/create-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "https://raw.githubusercontent.com/cs109/2014_data/master/countries.csv",
  "method": "filecount"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/splitCSV/latest/actions/create-order', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file": "https://raw.githubusercontent.com/cs109/2014_data/master/countries.csv",
    "method": "filecount"
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
      "id": "string",
      "order": {
        "created": "2026-05-07T12:00:00.000Z",
        "id": "string",
        "name": "Ava Chen"
      },
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Create Order action reference](actions/create-order.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/splitCSV/latest/actions/create-order).
