# EchtPost Postcards Universal API Examples

These examples use the MindCloud API key and EchtPost Postcards connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Credits

Retrieves your account balance from EchtPost Postcards.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/echtPostPostcards/latest/actions/get-credits?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/echtPostPostcards/latest/actions/get-credits?${params}`, {
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

See the full [Get Credits action reference](actions/get-credits.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/echtPostPostcards/latest/actions/get-credits).

## Add Credits

Adds postcard credits to your EchtPost Postcards account.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/echtPostPostcards/latest/actions/add-credits" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "numberCards": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/echtPostPostcards/latest/actions/add-credits', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "numberCards": 1
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

See the full [Add Credits action reference](actions/add-credits.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/echtPostPostcards/latest/actions/add-credits).
