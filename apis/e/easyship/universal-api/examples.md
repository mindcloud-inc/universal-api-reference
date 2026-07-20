# Easyship Universal API Examples

These examples use the MindCloud API key and Easyship connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Account Information

Retrieves current account information from Easyship.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/easyship/latest/actions/get-account-information?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/easyship/latest/actions/get-account-information?${params}`, {
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
      "billingAddress": {
        "city": "string",
        "companyName": "Ava Chen",
        "contactEmail": "ava@example.com",
        "contactName": "Ava Chen",
        "contactPhone": "string",
        "countryAlpha2": "string",
        "defaultFor": {
          "billing": true,
          "pickup": true,
          "return": true,
          "sender": true
        },
        "id": "string",
        "line1": "string",
        "line2": "string",
        "postalCode": "string",
        "state": "string",
        "status": "string"
      },
      "credit": {
        "availableBalance": 1,
        "balance": 1,
        "currency": "string"
      },
      "easyshipCompanyId": "string",
      "name": "Ava Chen",
      "paymentSources": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [Get Account Information action reference](actions/get-account-information.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/easyship/latest/actions/get-account-information).

## Cancel Pickup

Cancels a pickup in Easyship.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/easyship/latest/actions/cancel-pickup" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "pickupId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/easyship/latest/actions/cancel-pickup', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "pickupId": "string"
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
      "meta": {
        "requestId": "string"
      },
      "success": {
        "message": "string"
      }
    }
  ],
  "meta": {}
}
```

See the full [Cancel Pickup action reference](actions/cancel-pickup.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/easyship/latest/actions/cancel-pickup).
