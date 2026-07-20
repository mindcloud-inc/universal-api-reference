# Timelink Universal API Examples

These examples use the MindCloud API key and Timelink connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Company

Retrieves company details from the Timelink workspace.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timelink/latest/actions/get-company?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timelink/latest/actions/get-company?${params}`, {
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
      "activeClientsCount": 1,
      "activeProjectsCount": 1,
      "activeServicesCount": 1,
      "activeUsersCount": 1,
      "address": "string",
      "autoupdateQuantity": true,
      "city": "string",
      "color": {},
      "country": {},
      "createdAt": "string",
      "deletedAt": {},
      "disabledClientsCount": 1,
      "disabledProjectsCount": 1,
      "disabledServicesCount": 1,
      "email": "ava@example.com",
      "forceOauth": true,
      "hasDemoData": true,
      "id": "string",
      "industry": "string",
      "invoiceEmail": "ava@example.com",
      "language": {},
      "licenses": 1,
      "logo": {},
      "name": "Ava Chen",
      "oauth": {},
      "oauthProvider": {},
      "phone": "string",
      "pullProvider": {},
      "pushIntegration": {},
      "pushProvider": {},
      "requiredFields": [
        "string"
      ],
      "settings": {},
      "sizeOfCompany": "string",
      "stripeExists": true,
      "subscription": {
        "endsAt": {},
        "pastDue": {},
        "product": "string",
        "quantity": {},
        "status": "string",
        "trial": true,
        "trialEndsAt": "string"
      },
      "trialEndsAt": "string",
      "updatedAt": "string",
      "usersCount": 1,
      "vatid": {},
      "zip": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Company action reference](actions/get-company.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/timelink/latest/actions/get-company).

## Create Client

Creates a client in the Timelink workspace.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/timelink/latest/actions/create-client" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/timelink/latest/actions/create-client', {
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
      "color": "string",
      "company": {
        "address": "string",
        "autoupdateQuantity": true,
        "city": "string",
        "color": {},
        "country": {},
        "createdAt": "string",
        "deletedAt": {},
        "email": "ava@example.com",
        "forceOauth": true,
        "hasDemoData": true,
        "id": "string",
        "industry": "string",
        "invoiceEmail": "ava@example.com",
        "language": {},
        "licenses": 1,
        "logo": {},
        "name": "Ava Chen",
        "oauth": {},
        "oauthProvider": {},
        "phone": "string",
        "pullProvider": {},
        "pushIntegration": {},
        "pushProvider": {},
        "requiredFields": [
          "string"
        ],
        "settings": {},
        "sizeOfCompany": "string",
        "stripeExists": true,
        "subscription": {
          "endsAt": {},
          "pastDue": {},
          "product": "string",
          "quantity": {},
          "status": "string",
          "trial": true,
          "trialEndsAt": "string"
        },
        "trialEndsAt": "string",
        "updatedAt": "string",
        "vatid": {},
        "zip": "string"
      },
      "companyId": "string",
      "createdAt": "string",
      "extToolId": "string",
      "id": "string",
      "name": "Ava Chen",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Client action reference](actions/create-client.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/timelink/latest/actions/create-client).
