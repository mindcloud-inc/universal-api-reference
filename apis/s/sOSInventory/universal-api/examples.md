# SOS Inventory Universal API Examples

These examples use the MindCloud API key and SOS Inventory connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Locations

Retrieves locations from SOS Inventory.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sOSInventory/latest/actions/list-locations?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sOSInventory/latest/actions/list-locations?${params}`, {
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
      "address": {
        "city": {},
        "country": {},
        "line1": {},
        "line2": {},
        "line3": {},
        "line4": {},
        "line5": {},
        "postalCode": {},
        "stateProvince": {}
      },
      "binTracking": true,
      "company": {},
      "contact": {},
      "defaultLocation": true,
      "email": {},
      "id": 1,
      "keys": {},
      "name": "Ava Chen",
      "nonNettable": true,
      "phone": {},
      "salesTaxRate": 1,
      "shippingTaxable": true,
      "syncToken": 1,
      "values": {}
    }
  ],
  "meta": {}
}
```

See the full [List Locations action reference](actions/list-locations.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sOSInventory/latest/actions/list-locations).

## Create Customer

Creates a customer in SOS Inventory.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sOSInventory/latest/actions/create-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sOSInventory/latest/actions/create-customer', {
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
      "altPhone": "string",
      "archived": true,
      "billing": {
        "city": {},
        "country": {},
        "line1": {},
        "line2": {},
        "line3": {},
        "line4": {},
        "line5": {},
        "postalCode": {},
        "stateProvince": {}
      },
      "billWithParent": true,
      "businessLicense": "string",
      "companyName": "Ava Chen",
      "contact": {
        "firstName": {},
        "lastName": {},
        "middleName": {},
        "suffix": {},
        "title": {}
      },
      "contractorNumber": "string",
      "creditHold": true,
      "currency": {},
      "customerType": {},
      "customFields": {},
      "email": "ava@example.com",
      "expMonth": {},
      "expYear": {},
      "fax": "string",
      "foundUsVia": "string",
      "fullname": "Ava Chen",
      "hasCardOnFile": true,
      "hasChildren": true,
      "id": 1,
      "isInQuickBooks": true,
      "keys": {},
      "lastFour": {},
      "lastSync": "string",
      "mobile": "string",
      "name": "Ava Chen",
      "notes": "string",
      "parent": {},
      "paymentMethod": {},
      "phone": "string",
      "portalPassword": "string",
      "priceTier": {},
      "resaleNumber": "string",
      "salesRep": {},
      "shipping": {
        "city": {},
        "country": {},
        "line1": {},
        "line2": {},
        "line3": {},
        "line4": {},
        "line5": {},
        "postalCode": {},
        "stateProvince": {}
      },
      "starred": 1,
      "sublevel": 1,
      "summaryOnly": true,
      "syncMessage": {},
      "syncToken": 1,
      "tax": {
        "taxable": true,
        "taxCode": {},
        "taxExemptReasonId": {}
      },
      "terms": {},
      "tokenType": {},
      "values": {},
      "website": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Customer action reference](actions/create-customer.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sOSInventory/latest/actions/create-customer).
