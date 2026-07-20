# ServiceTitan Universal API Examples

These examples use the MindCloud API key and ServiceTitan connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Activity Codes

Retrieves activity codes from ServiceTitan.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/list-activity-codes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/list-activity-codes?${params}`, {
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
  "data": [],
  "meta": {}
}
```

See the full [List Activity Codes action reference](actions/list-activity-codes.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/servicetitan/latest/actions/list-activity-codes).

## Create Booking



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/create-booking" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "summary": "string",
  "name": "Ava Chen",
  "externalId": "string",
  "isFirstTimeClient": true,
  "source": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/create-booking', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "summary": "string",
    "name": "Ava Chen",
    "externalId": "string",
    "isFirstTimeClient": true,
    "source": "string"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [],
  "meta": {}
}
```

See the full [Create Booking action reference](actions/create-booking.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/servicetitan/latest/actions/create-booking).
