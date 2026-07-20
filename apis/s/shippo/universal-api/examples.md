# Shippo - Legacy Universal API Examples

These examples use the MindCloud API key and Shippo - Legacy connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Carrier Accounts

Retrieves carrier accounts connected to your Shippo account.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shippo/latest/actions/list-carrier-accounts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shippo/latest/actions/list-carrier-accounts?${params}`, {
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
      "next": "string",
      "previous": {},
      "results": [
        {
          "accountId": "string",
          "active": true,
          "carrier": "string",
          "carrierImages": {
            "75": "string",
            "200": "string"
          },
          "carrierName": "Ava Chen",
          "isShippoAccount": true,
          "metadata": "string",
          "objectId": "string",
          "objectInfo": {
            "authentication": {
              "type": "string"
            }
          },
          "objectOwner": "string",
          "test": true
        }
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Carrier Accounts action reference](actions/list-carrier-accounts.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/shippo/latest/actions/list-carrier-accounts).

## Create Insta Label

Creates a shipping label in one Shippo API call.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/shippo/latest/actions/create-insta-label" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/shippo/latest/actions/create-insta-label', {
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
      "commercialInvoiceUrl": {},
      "createdBy": {},
      "eta": {},
      "labelUrl": "https://example.com",
      "metadata": "string",
      "objectCreated": "string",
      "objectId": "string",
      "objectOwner": "string",
      "objectState": "string",
      "objectUpdated": "string",
      "order": {},
      "parcel": "string",
      "qrCodeUrl": {},
      "rate": {
        "amount": "string",
        "amountLocal": "string",
        "carrierAccount": "string",
        "currency": "string",
        "currencyLocal": "string",
        "objectId": "string",
        "provider": "string",
        "servicelevelName": "Ava Chen",
        "servicelevelToken": "string"
      },
      "status": "string",
      "test": true,
      "trackingNumber": "string",
      "trackingStatus": "string",
      "trackingUrlProvider": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Create Insta Label action reference](actions/create-insta-label.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/shippo/latest/actions/create-insta-label).
