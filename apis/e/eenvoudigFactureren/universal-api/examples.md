# EenvoudigFactureren Universal API Examples

These examples use the MindCloud API key and EenvoudigFactureren connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current Account

Retrieves the current account from EenvoudigFactureren.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eenvoudigFactureren/latest/actions/get-current-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eenvoudigFactureren/latest/actions/get-current-account?${params}`, {
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
      "account_id": 1,
      "account_type": "string",
      "account_type_until": "2026-05-07T12:00:00.000Z",
      "city": "string",
      "company_id": "string",
      "company_name": "Ava Chen",
      "country": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "email_address": "ava@example.com",
      "language": "string",
      "last_login": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "number": "string",
      "postal_code": "string",
      "street": "string",
      "vat_number": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Current Account action reference](actions/get-current-account.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/eenvoudigFactureren/latest/actions/get-current-account).

## Create Client

Creates a new client in EenvoudigFactureren.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/eenvoudigFactureren/latest/actions/create-client" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eenvoudigFactureren/latest/actions/create-client', {
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
      "city": "string",
      "client_id": 1,
      "country": "string",
      "email_address": "ava@example.com",
      "last_activity": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "number": "string",
      "phone_number": "string",
      "postal_code": "string",
      "state": "string",
      "street": "string",
      "uri": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Client action reference](actions/create-client.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/eenvoudigFactureren/latest/actions/create-client).
