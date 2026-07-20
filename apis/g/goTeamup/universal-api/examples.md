# GoTeamup Universal API Examples

These examples use the MindCloud API key and GoTeamup connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Providers

Finds providers in GoTeamup.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goTeamup/latest/actions/list-providers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goTeamup/latest/actions/list-providers?${params}`, {
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
      "country": "string",
      "currency": {
        "isoCurrencyCode": "string",
        "position": "string",
        "symbol": "string"
      },
      "description": "string",
      "id": 1,
      "isMarketingPreferenceOnCustomerForms": true,
      "logo": {
        "originalHeight": {},
        "originalWidth": {},
        "url": "https://example.com"
      },
      "name": "Ava Chen",
      "object": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Providers action reference](actions/list-providers.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/goTeamup/latest/actions/list-providers).

## Cancel Customer Membership

Cancels an existing customer membership in GoTeamup.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/goTeamup/latest/actions/cancel-customer-membership" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/goTeamup/latest/actions/cancel-customer-membership', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
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
      "activeHold": {},
      "billedPrice": {},
      "cancellationReason": "string",
      "customer": 1,
      "discountCode": {},
      "discountCodeMakesFreeForever": true,
      "expirationDate": "string",
      "id": 1,
      "isSetForCancellation": true,
      "membership": 1,
      "name": "Ava Chen",
      "object": "string",
      "paymentSubscription": {},
      "renewalDate": {},
      "startDate": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Cancel Customer Membership action reference](actions/cancel-customer-membership.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/goTeamup/latest/actions/cancel-customer-membership).
