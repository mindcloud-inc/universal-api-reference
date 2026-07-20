# Viewpoint Spectrum Universal API Examples

These examples use the MindCloud API key and Viewpoint Spectrum connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Vendors



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/viewpointSpectrum/latest/actions/list-vendors?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/viewpointSpectrum/latest/actions/list-vendors?${params}`, {
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
      "accountReference": "string",
      "address1": "string",
      "address2": "string",
      "city": "string",
      "companyCode": "string",
      "discountPercent": 1,
      "discountTermDays": 1,
      "discountTerms": "string",
      "email": "ava@example.com",
      "firstName": "Ava",
      "lastName": "Chen",
      "name": "Ava Chen",
      "paymentAddress1": "string",
      "paymentAddress2": "string",
      "paymentCity": "string",
      "paymentLocationName": "Ava Chen",
      "paymentState": "string",
      "paymentTermDays": 1,
      "paymentTerms": "string",
      "paymentZip": "string",
      "phone": "string",
      "purchaseAddress1": "string",
      "purchaseAddress2": "string",
      "purchaseCity": "string",
      "purchaseLocationName": "Ava Chen",
      "purchaseState": "string",
      "purchaseZip": "string",
      "state": "string",
      "vendorCode": "string",
      "zipCode": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Vendors action reference](actions/list-vendors.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/viewpointSpectrum/latest/actions/list-vendors).

## Create Customer



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/viewpointSpectrum/latest/actions/create-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customerCode": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/viewpointSpectrum/latest/actions/create-customer', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customerCode": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [],
  "meta": {}
}
```

See the full [Create Customer action reference](actions/create-customer.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/viewpointSpectrum/latest/actions/create-customer).
