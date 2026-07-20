# Goody Universal API Examples

These examples use the MindCloud API key and Goody connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current User

Retrieves the current user from Goody.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goody/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goody/latest/actions/get-current-user?${params}`, {
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
      "email": "ava@example.com",
      "public_app_id": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Current User action reference](actions/get-current-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/goody/latest/actions/get-current-user).

## Cancel Order

Cancels an order in Goody.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/goody/latest/actions/cancel-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/goody/latest/actions/cancel-order', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
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
      "amounts": {
        "amount_global_relay_cost": "string",
        "amount_pre_tax_total": 1,
        "amount_processing_fee": 1,
        "amount_product": 1,
        "amount_shipping": 1,
        "amount_tax": "string",
        "amount_total": "string"
      },
      "card_id": "string",
      "cart": {
        "id": "string",
        "items": {
          "id": "string",
          "product": {
            "brand": {},
            "id": "string",
            "name": "Ava Chen"
          },
          "quantity": 1
        }
      },
      "expires_at": "string",
      "id": "string",
      "individual_gift_link": "https://example.com",
      "is_swapped": true,
      "message": "string",
      "order_batch_id": "string",
      "original_amounts": "string",
      "original_cart": "string",
      "recipient_email": "ava@example.com",
      "recipient_first_name": "Ava",
      "recipient_last_name": "Chen",
      "reference_id": "string",
      "sender": {
        "email": "ava@example.com",
        "first_name": "Ava",
        "last_name": "Chen"
      },
      "shipments": [
        "string"
      ],
      "status": "string",
      "thank_you_note": "string",
      "view_count_recipient": 1,
      "workspace_id": "string",
      "workspace_name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Cancel Order action reference](actions/cancel-order.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/goody/latest/actions/cancel-order).
