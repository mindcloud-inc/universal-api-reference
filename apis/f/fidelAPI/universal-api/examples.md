# Fidel API Universal API Examples

These examples use the MindCloud API key and Fidel API connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Brands

Retrieves brands from Fidel API.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fidelAPI/latest/actions/list-brands?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fidelAPI/latest/actions/list-brands?${params}`, {
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
      "accountId": "string",
      "consent": true,
      "created": "string",
      "id": "string",
      "live": true,
      "name": "Ava Chen",
      "updated": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Brands action reference](actions/list-brands.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/fidelAPI/latest/actions/list-brands).

## Activate Offer on Card

Activates an offer on a Fidel card.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fidelAPI/latest/actions/activate-offer-on-card" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "offerId": "string",
  "cardId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fidelAPI/latest/actions/activate-offer-on-card', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "offerId": "string",
    "cardId": "string"
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
      "execution": 1,
      "resource": "string",
      "status": 1
    }
  ],
  "meta": {}
}
```

See the full [Activate Offer on Card action reference](actions/activate-offer-on-card.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/fidelAPI/latest/actions/activate-offer-on-card).
