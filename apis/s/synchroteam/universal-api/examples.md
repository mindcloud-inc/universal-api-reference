# Synchroteam Universal API Examples

These examples use the MindCloud API key and Synchroteam connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Customers

Retrieves customers from Synchroteam, optionally filtered by change date.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/synchroteam/latest/actions/list-customers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/synchroteam/latest/actions/list-customers?${params}`, {
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
      "Address": "string",
      "AddressComplement": "string",
      "AdressCity": "string",
      "AdressCountry": "string",
      "AdressStreet": "string",
      "AdressZIP": "string",
      "ContactEmail": "ava@example.com",
      "ContactFax": "string",
      "ContactFirstName": "Ava",
      "ContactMobile": "string",
      "ContactName": "Ava Chen",
      "ContactPhone": "string",
      "id": 1,
      "MyId": "string",
      "Name": "Ava Chen",
      "Position": {},
      "publicLink": "https://example.com",
      "VatNumber": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Customers action reference](actions/list-customers.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/synchroteam/latest/actions/list-customers).

## Cancel Job

Cancels a job in Synchroteam by supported identifier.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/synchroteam/latest/actions/cancel-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "identifierType": "string",
  "identifierValue": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/synchroteam/latest/actions/cancel-job', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "identifierType": "string",
    "identifierValue": "string"
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
      "code": 1,
      "message": "string"
    }
  ],
  "meta": {}
}
```

See the full [Cancel Job action reference](actions/cancel-job.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/synchroteam/latest/actions/cancel-job).
