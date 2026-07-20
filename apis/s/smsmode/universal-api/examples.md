# smsmode Universal API Examples

These examples use the MindCloud API key and smsmode connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Organisations



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smsmode/latest/actions/list-organisations?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smsmode/latest/actions/list-organisations?${params}`, {
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
        "address1": "string",
        "address2": "string",
        "city": "string",
        "country": "string",
        "zipCode": "string"
      },
      "balance": {
        "amount": 1,
        "currency": "string",
        "parentBilling": true,
        "paymentType": "string"
      },
      "billingAddress": {
        "address1": "string",
        "address2": "string",
        "city": "string",
        "country": "string",
        "zipCode": "string"
      },
      "billingContact": {
        "email": "ava@example.com",
        "firstName": "Ava",
        "lastName": "Chen",
        "mobile": "string"
      },
      "companyInformation": {
        "name": "Ava Chen",
        "registrationNumber": "string",
        "vatNumber": "string",
        "website": "string"
      },
      "contact": {
        "email": "ava@example.com",
        "firstName": "Ava",
        "lastName": "Chen",
        "mobile": "string"
      },
      "creationDate": "2026-05-07T12:00:00.000Z",
      "href": "string",
      "monthlyConsumption": 1,
      "monthlyConsumptionLimit": 1,
      "name": "Ava Chen",
      "organisationId": "string",
      "parentOrganisationId": "string",
      "state": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Organisations action reference](actions/list-organisations.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/smsmode/latest/actions/list-organisations).

## Create Channel



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/smsmode/latest/actions/create-channel" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "organisationId": "string",
  "name": "Ava Chen",
  "type": "string",
  "flow": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/smsmode/latest/actions/create-channel', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "organisationId": "string",
    "name": "Ava Chen",
    "type": "string",
    "flow": "string"
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
      "dailyConsumptionLimit": 1,
      "defaultCallbackUrlMo": "https://example.com",
      "defaultCallbackUrlStatus": "https://example.com",
      "flow": "string",
      "name": "Ava Chen",
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Channel action reference](actions/create-channel.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/smsmode/latest/actions/create-channel).
