# Middesk Universal API Examples

These examples use the MindCloud API key and Middesk connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get TIN Match Availability

Retrieves TIN match availability from Middesk.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/middesk/latest/actions/get-tin-match-availability?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/middesk/latest/actions/get-tin-match-availability?${params}`, {
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
      "available": true
    }
  ],
  "meta": {}
}
```

See the full [Get TIN Match Availability action reference](actions/get-tin-match-availability.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/middesk/latest/actions/get-tin-match-availability).

## Autocomplete business identities

Autocompletes business identities in your Middesk account.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/middesk/latest/actions/autocomplete-business-identities" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/middesk/latest/actions/autocomplete-business-identities', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
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
      "data": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [Autocomplete business identities action reference](actions/autocomplete-business-identities.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/middesk/latest/actions/autocomplete-business-identities).
