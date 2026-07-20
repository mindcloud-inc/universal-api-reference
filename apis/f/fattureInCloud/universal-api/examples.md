# Fatture in Cloud Universal API Examples

These examples use the MindCloud API key and Fatture in Cloud connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List User Companies

Retrieves the user's companies from Fatture in Cloud.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fattureInCloud/latest/actions/list-user-companies?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fattureInCloud/latest/actions/list-user-companies?${params}`, {
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
      "connectionId": 1,
      "connectionRole": "string",
      "dic": true,
      "dicPlan": 1,
      "email": "ava@example.com",
      "fic": true,
      "ficLicenseExpire": "2026-05-07T12:00:00.000Z",
      "ficPlan": "string",
      "id": 1,
      "name": "Ava Chen",
      "permissions": {
        "dicEmployees": "string",
        "dicSettings": "string",
        "dicTimesheet": "string",
        "ficArchive": "string",
        "ficCalendar": "string",
        "ficCashbook": "string",
        "ficClients": "string",
        "ficEmails": "ava@example.com",
        "ficIssuedDocuments": "string",
        "ficProducts": "string",
        "ficReceipts": "string",
        "ficReceivedDocuments": "string",
        "ficSettings": "string",
        "ficSituation": "string",
        "ficStock": "string",
        "ficSuppliers": "string",
        "ficTaxes": "string"
      },
      "taxCode": "string",
      "type": "string",
      "vatNumber": "string"
    }
  ],
  "meta": {}
}
```

See the full [List User Companies action reference](actions/list-user-companies.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/fattureInCloud/latest/actions/list-user-companies).

## Create Client

Creates a new client in Fatture in Cloud.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fattureInCloud/latest/actions/create-client" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "companyId": 1,
  "data": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fattureInCloud/latest/actions/create-client', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "companyId": 1,
    "data": {}
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
      "addressCity": "string",
      "addressExtra": "string",
      "addressPostalCode": "string",
      "addressProvince": "string",
      "addressStreet": "string",
      "bankIban": "string",
      "bankName": "Ava Chen",
      "bankSwiftCode": "string",
      "certifiedEmail": "ava@example.com",
      "code": "string",
      "contactPerson": "string",
      "country": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "defaultPaymentMethod": {
        "id": 1,
        "name": "Ava Chen"
      },
      "defaultPaymentTerms": 1,
      "defaultPaymentTermsType": "string",
      "defaultVat": {
        "description": "string",
        "id": 1,
        "isDisabled": true,
        "value": 1
      },
      "eiCode": "string",
      "eInvoice": true,
      "email": "ava@example.com",
      "fax": "string",
      "firstName": "Ava",
      "id": 1,
      "lastName": "Chen",
      "name": "Ava Chen",
      "notes": "string",
      "phone": "string",
      "shippingAddress": "string",
      "taxCode": "string",
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "vatNumber": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Client action reference](actions/create-client.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/fattureInCloud/latest/actions/create-client).
