# ProProfs Project Universal API Examples

These examples use the MindCloud API key and ProProfs Project connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Company

Retrieves company details from ProProfs Project.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/proProfsProject/latest/actions/get-company?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/proProfsProject/latest/actions/get-company?${params}`, {
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
      "address1": "string",
      "address2": "string",
      "autoIds": "string",
      "billingEmail": "ava@example.com",
      "city": "string",
      "companyId": "string",
      "companyName": "Ava Chen",
      "country": "string",
      "currency": "string",
      "customCss": "string",
      "customHeaderBg": "string",
      "dateCreated": "string",
      "dateOrder": "string",
      "defaultOrder": "string",
      "domain": "string",
      "estimateEmailTemplate": "ava@example.com",
      "estimateFooter": "string",
      "firstDay": "string",
      "invoiceEmailTemplate": "ava@example.com",
      "invoiceFooter": "string",
      "language": "string",
      "logo": "string",
      "phone": "string",
      "postcode": "string",
      "progressType": "string",
      "roundBillableHours": "string",
      "signature": "string",
      "state": "string",
      "superuserId": "string",
      "timezone": "string",
      "users": [
        {
          "userId": "string",
          "userName": "Ava Chen"
        }
      ]
    }
  ],
  "meta": {}
}
```

See the full [Get Company action reference](actions/get-company.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/proProfsProject/latest/actions/get-company).

## Create Client

Creates a new client in ProProfs Project.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/proProfsProject/latest/actions/create-client" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "clientName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/proProfsProject/latest/actions/create-client', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "clientName": "Ava Chen"
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
      "active": "string",
      "address": "string",
      "background": "string",
      "city": "string",
      "clientId": "string",
      "clientName": "Ava Chen",
      "contactId": "string",
      "country": "string",
      "dateCreated": "string",
      "dateModified": "string",
      "email": "ava@example.com",
      "fax": "string",
      "mobile": "string",
      "postcode": "string",
      "state": "string",
      "tel": "string",
      "userId": "string",
      "website": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Client action reference](actions/create-client.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/proProfsProject/latest/actions/create-client).
