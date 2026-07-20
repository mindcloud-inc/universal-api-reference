# ReadyCloud Suite Universal API Examples

These examples use the MindCloud API key and ReadyCloud Suite connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Organizations

Retrieves organizations from ReadyCloud Suite.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/readyCloudSuite/latest/actions/list-organizations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/readyCloudSuite/latest/actions/list-organizations?${params}`, {
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
      "action_alert_custom_domain_enabled": true,
      "action_alert_send_from_alias": "string",
      "app_seat_licenses": [
        {}
      ],
      "avatar": "string",
      "billing_status": "string",
      "cached_orders_views": true,
      "deleted_at": "2026-05-07T12:00:00.000Z",
      "equipment_returns_enabled": true,
      "fees_paid_by": "string",
      "member_websocket_channel_id": "string",
      "name": "Ava Chen",
      "payment_plan": {},
      "subscriptions": {},
      "trial_expires_at": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com",
      "user_slots": 1,
      "wallet_auto_refill_amount": 1,
      "wallet_auto_refill_limit": 1,
      "wallet_charges_allowed": true,
      "website": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Organizations action reference](actions/list-organizations.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/readyCloudSuite/latest/actions/list-organizations).

## Create Box

Creates a new box in ReadyCloud Suite.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/readyCloudSuite/latest/actions/create-box" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "orderPk": "string",
  "orgPk": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/readyCloudSuite/latest/actions/create-box', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "orderPk": "string",
    "orgPk": "string"
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
      "cod": true,
      "cod_value": "string",
      "confirmation_type": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "custom_fields": {},
      "declared_value": "string",
      "delivered_at": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "height": 1,
      "insurance_type": "string",
      "insured_value": "string",
      "items": [
        {}
      ],
      "length": 1,
      "package_type": "string",
      "packaging": {},
      "saturday_delivery": true,
      "ship_cost": "string",
      "shipper_release": true,
      "shipping_docs": [
        {}
      ],
      "tracking": [
        {}
      ],
      "tracking_number": "string",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com",
      "weight": "string",
      "width": 1
    }
  ],
  "meta": {}
}
```

See the full [Create Box action reference](actions/create-box.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/readyCloudSuite/latest/actions/create-box).
