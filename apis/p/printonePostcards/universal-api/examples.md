# Print.one Postcards Universal API Examples

These examples use the MindCloud API key and Print.one Postcards connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get My Company

Retrieves your company details from Print.one Postcards.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/printonePostcards/latest/actions/get-my-company?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/printonePostcards/latest/actions/get-my-company?${params}`, {
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
      "canBeBilled": true,
      "city": "string",
      "cocNumber": "string",
      "companyName": "Ava Chen",
      "country": "string",
      "createdAt": "string",
      "email": "ava@example.com",
      "emailVerifiedAt": "ava@example.com",
      "financialContactEmail": "ava@example.com",
      "financialContactName": "Ava Chen",
      "firstName": "Ava",
      "forceTwoFactor": true,
      "houseNumber": "string",
      "iban": "string",
      "id": "string",
      "invoiceEmail": "ava@example.com",
      "invoicingPolicy": "string",
      "lastLoginAt": "string",
      "lastName": "Chen",
      "phoneNumber": "string",
      "phonePrefix": "string",
      "planId": "string",
      "postalCode": "string",
      "postpaidLimit": 1,
      "region": "string",
      "returnAddressee": "string",
      "returnCity": "string",
      "returnCountry": "string",
      "returnHouseNumber": "string",
      "returnPostalCode": "string",
      "returnStreet": "string",
      "secondAddressLine": "string",
      "street": "string",
      "technicalContactEmail": "ava@example.com",
      "technicalContactName": "Ava Chen",
      "updatedAt": "string",
      "vatNumber": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get My Company action reference](actions/get-my-company.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/printonePostcards/latest/actions/get-my-company).

## Add Orders To Batch

Adds orders to a batch in Print.one Postcards.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/printonePostcards/latest/actions/add-orders-to-batch" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "batchId": "string",
  "mergeVariables": {},
  "recipient.name": "Ava Chen",
  "recipient.address": "string",
  "recipient.postalCode": "string",
  "recipient.city": "string",
  "recipient.country": "NL"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/printonePostcards/latest/actions/add-orders-to-batch', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "batchId": "string",
    "mergeVariables": {},
    "recipient.name": "Ava Chen",
    "recipient.address": "string",
    "recipient.postalCode": "string",
    "recipient.city": "string",
    "recipient.country": "NL"
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
      "batchId": "string",
      "companyId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "csvOrderId": "string",
      "errors": [
        "string"
      ],
      "finish": "string",
      "format": "string",
      "friendlyStatus": "string",
      "id": "string",
      "mergeVariables": {},
      "metadata": {},
      "recipient": {},
      "sendDate": "2026-05-07T12:00:00.000Z",
      "sender": {},
      "status": "string",
      "templateId": "string",
      "templateVersion": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "warnings": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

See the full [Add Orders To Batch action reference](actions/add-orders-to-batch.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/printonePostcards/latest/actions/add-orders-to-batch).
