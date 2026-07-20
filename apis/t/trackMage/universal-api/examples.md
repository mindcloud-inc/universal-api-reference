# TrackMage Universal API Examples

These examples use the MindCloud API key and TrackMage connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Workspaces

Retrieves workspaces from your TrackMage account.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trackMage/latest/actions/list-workspaces?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trackMage/latest/actions/list-workspaces?${params}`, {
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
      "considerShipmentDelayed": {},
      "defaultTrackingPage": "string",
      "ecommerceIntegrationType": "string",
      "emailSettings": {},
      "id": "string",
      "logo": {
        "filePath": "string",
        "id": "string",
        "thumbnailPath": "string"
      },
      "members": [
        "string"
      ],
      "ordersCount": 1,
      "preferredCarriers": [
        "string"
      ],
      "scheduledForDelete": true,
      "shipmentsCount": 1,
      "team": "string",
      "title": "string",
      "widgets": [
        "string"
      ],
      "workflowsCount": 1,
      "workflowsOrder": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Workspaces action reference](actions/list-workspaces.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/trackMage/latest/actions/list-workspaces).

## Create Order

Creates a new order in TrackMage.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/trackMage/latest/actions/create-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspace": "string",
  "orderNumber": "string",
  "orderType": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/trackMage/latest/actions/create-order', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspace": "string",
    "orderNumber": "string",
    "orderType": "string"
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
      "billingAddress": {
        "addressLine1": "string",
        "addressLine2": "string",
        "city": "string",
        "company": "string",
        "country": "string",
        "countryIso2": "string",
        "firstName": "Ava",
        "lastName": "Chen",
        "postcode": "string",
        "state": "string"
      },
      "createdAt": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "email": "ava@example.com",
      "externalSourceIntegration": "string",
      "externalSourceIntegrationType": "string",
      "externalSourceSyncId": "string",
      "externalSourceUrl": "https://example.com",
      "fulfillmentStatus": "string",
      "id": "string",
      "orderNumber": "string",
      "orderStatus": {
        "code": "string",
        "description": "string",
        "id": "string",
        "title": "string"
      },
      "orderType": "string",
      "phoneNumber": "string",
      "readonly": true,
      "shipments": [
        "string"
      ],
      "shipmentsWithoutTrackingCount": 1,
      "shippingAddress": {
        "addressLine1": "string",
        "addressLine2": "string",
        "city": "string",
        "company": "string",
        "country": "string",
        "countryIso2": "string",
        "firstName": "Ava",
        "lastName": "Chen",
        "postcode": "string",
        "state": "string"
      },
      "subtotal": "string",
      "total": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "workspace": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Order action reference](actions/create-order.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/trackMage/latest/actions/create-order).
