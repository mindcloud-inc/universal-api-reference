# RunSignup Universal API Examples

These examples use the MindCloud API key and RunSignup connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Races



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/runSignup/latest/actions/list-races?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/runSignup/latest/actions/list-races?${params}`, {
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

See the full [List Races action reference](actions/list-races.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/runSignup/latest/actions/list-races).

## Add or Edit Coupon



```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/runSignup/latest/actions/add-or-edit-coupon" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "raceId": "string",
  "request": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/runSignup/latest/actions/add-or-edit-coupon', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "raceId": "string",
    "request": "string"
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

See the full [Add or Edit Coupon action reference](actions/add-or-edit-coupon.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/runSignup/latest/actions/add-or-edit-coupon).
