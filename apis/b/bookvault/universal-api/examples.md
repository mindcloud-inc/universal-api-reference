# Bookvault Universal API Examples

These examples use the MindCloud API key and Bookvault connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Account

Retrieves your account details from Bookvault.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bookvault/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bookvault/latest/actions/get-account?${params}`, {
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
      "Email": "ava@example.com",
      "FirstName": "Ava",
      "IsDisabled": true,
      "LastName": "Chen",
      "Phone": "string",
      "ProfileID": 1,
      "Role": {}
    }
  ],
  "meta": {}
}
```

See the full [Get Account action reference](actions/get-account.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/bookvault/latest/actions/get-account).

## Create Address

Creates a new address in Bookvault.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bookvault/latest/actions/create-address" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "address": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bookvault/latest/actions/create-address', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "address": {}
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
      "Address1": "string",
      "Addressee": "string",
      "CommonAddrID": 1,
      "Company": "string",
      "Country": {},
      "Email": "ava@example.com",
      "Postcode": "string",
      "Town": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Address action reference](actions/create-address.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/bookvault/latest/actions/create-address).
