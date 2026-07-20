# ServiceM8 Universal API Examples

These examples use the MindCloud API key and ServiceM8 connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Clients



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/serviceM8/latest/actions/list-clients?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/serviceM8/latest/actions/list-clients?${params}`, {
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
      "abnNumber": "string",
      "active": 1,
      "address": "string",
      "addressCity": "string",
      "addressCountry": "string",
      "addressPostcode": "string",
      "addressState": "string",
      "addressStreet": "string",
      "badges": "string",
      "billingAddress": "string",
      "billingAttention": "string",
      "editDate": "2026-05-07T12:00:00.000Z",
      "faxNumber": "string",
      "isIndividual": 1,
      "name": "Ava Chen",
      "paymentTerms": "string",
      "taxRateUuid": "string",
      "uuid": "string",
      "website": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Clients action reference](actions/list-clients.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/serviceM8/latest/actions/list-clients).

## Create Client



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/serviceM8/latest/actions/create-client" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/serviceM8/latest/actions/create-client', {
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
      "recordUuid": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Client action reference](actions/create-client.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/serviceM8/latest/actions/create-client).
