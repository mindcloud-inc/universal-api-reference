# Zoho Billing Universal API Examples

These examples use the MindCloud API key and Zoho Billing connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Organizations



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoBilling/latest/actions/list-organizations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoBilling/latest/actions/list-organizations?${params}`, {
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
      "code": 1,
      "message": "string",
      "organizations": [
        [
          {}
        ]
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Organizations action reference](actions/list-organizations.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/zohoBilling/latest/actions/list-organizations).

## Cancel Subscription



```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zohoBilling/latest/actions/cancel-subscription" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "subscriptionId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoBilling/latest/actions/cancel-subscription', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "subscriptionId": "string"
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
      "code": 1,
      "message": "string",
      "subscription": {
        "activated_at": "2026-05-07T12:00:00.000Z",
        "addons": [
          [
            {}
          ]
        ],
        "amount": 1,
        "auto_collect": true,
        "billing_mode": "string",
        "created_at": "2026-05-07T12:00:00.000Z",
        "current_term_ends_at": "2026-05-07T12:00:00.000Z",
        "current_term_starts_at": "2026-05-07T12:00:00.000Z",
        "customer": {
          "customer_id": "string",
          "display_name": "Ava Chen",
          "email": "ava@example.com"
        },
        "customer_id": "string",
        "line_items": [
          [
            {}
          ]
        ],
        "name": "Ava Chen",
        "next_billing_at": "2026-05-07T12:00:00.000Z",
        "plan": {
          "name": "Ava Chen",
          "plan_code": "string",
          "plan_id": "string",
          "price": 1
        },
        "product_id": "string",
        "product_name": "Ava Chen",
        "status": "string",
        "subscription_id": "string",
        "subscription_number": "string",
        "taxes": [
          [
            {}
          ]
        ]
      }
    }
  ],
  "meta": {}
}
```

See the full [Cancel Subscription action reference](actions/cancel-subscription.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/zohoBilling/latest/actions/cancel-subscription).
