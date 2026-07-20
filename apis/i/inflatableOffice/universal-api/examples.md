# InflatableOffice Universal API Examples

These examples use the MindCloud API key and InflatableOffice connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Customers

Retrieves customers from InflatableOffice.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/inflatableOffice/latest/actions/list-customers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/inflatableOffice/latest/actions/list-customers?${params}`, {
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
      "aataxexempt": "string",
      "active": "string",
      "address2": "string",
      "cellphone": "string",
      "city": "string",
      "country": "string",
      "createtime": "string",
      "createtimeTs": "string",
      "createtimeUtc": "string",
      "customertype": "string",
      "email": "ava@example.com",
      "fax": "string",
      "fbprofileid": "string",
      "firstname": "Ava",
      "homephone": "string",
      "href": "string",
      "id": "string",
      "isblacklisted": "string",
      "lastactiontime": "string",
      "lastcontacttime": "string",
      "lastname": "Chen",
      "locationid": "string",
      "modifiedtime": "string",
      "modifiedtimeTs": "string",
      "modifiedtimeUtc": "string",
      "notes": "string",
      "officephone": "string",
      "oktotext": "string",
      "organization": "string",
      "qboid": "string",
      "qboname": "Ava Chen",
      "qbosendinvoice": "string",
      "qbosynctoken": "string",
      "qboupdatetime": "string",
      "referral": "string",
      "repeatcustomer": "string",
      "score": "string",
      "state": "string",
      "street": "string",
      "taxexemptid": "string",
      "title": "string",
      "zip": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Customers action reference](actions/list-customers.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/inflatableOffice/latest/actions/list-customers).

## Create Customer

Creates a new customer in InflatableOffice.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/inflatableOffice/latest/actions/create-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/inflatableOffice/latest/actions/create-customer', {
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
      "message": "string",
      "recordid": "string",
      "requestTime": 1,
      "status": 1
    }
  ],
  "meta": {}
}
```

See the full [Create Customer action reference](actions/create-customer.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/inflatableOffice/latest/actions/create-customer).
