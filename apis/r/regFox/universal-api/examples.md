# RegFox Universal API Examples

These examples use the MindCloud API key and RegFox connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Ping

Retrieves the RegFox API healthcheck response.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/regFox/latest/actions/ping?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/regFox/latest/actions/ping?${params}`, {
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
      "data": "string",
      "responseCode": 1
    }
  ],
  "meta": {}
}
```

See the full [Ping action reference](actions/ping.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/regFox/latest/actions/ping).

## Check In Registrant

Checks in a registrant in the RegFox account.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/regFox/latest/actions/check-in-registrant" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/regFox/latest/actions/check-in-registrant', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
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
      "date": "2026-05-07T12:00:00.000Z",
      "id": 1
    }
  ],
  "meta": {}
}
```

See the full [Check In Registrant action reference](actions/check-in-registrant.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/regFox/latest/actions/check-in-registrant).
