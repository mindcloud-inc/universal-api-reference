# Kiwify Universal API Examples

These examples use the MindCloud API key and Kiwify connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Payouts

Retrieves payouts from Kiwify.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kiwify/latest/actions/list-payouts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kiwify/latest/actions/list-payouts?${params}`, {
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
      "data": [
        "string"
      ],
      "pagination": {}
    }
  ],
  "meta": {}
}
```

See the full [List Payouts action reference](actions/list-payouts.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/kiwify/latest/actions/list-payouts).

## Create Payout

Creates a payout in Kiwify.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/kiwify/latest/actions/create-payout" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kiwify/latest/actions/create-payout', {
  method: 'POST',
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
      "id": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Payout action reference](actions/create-payout.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/kiwify/latest/actions/create-payout).
