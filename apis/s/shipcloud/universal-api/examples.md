# Shipcloud Universal API Examples

These examples use the MindCloud API key and Shipcloud connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current User

Retrieves the current user from Shipcloud.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shipcloud/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shipcloud/latest/actions/get-current-user?${params}`, {
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
      "customer_no": "string",
      "email": "ava@example.com",
      "environment": "string",
      "first_name": "Ava",
      "id": "string",
      "last_name": "Chen",
      "subscription": {}
    }
  ],
  "meta": {}
}
```

See the full [Get Current User action reference](actions/get-current-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/shipcloud/latest/actions/get-current-user).

## Create Address

Creates a new address in Shipcloud.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/shipcloud/latest/actions/create-address" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/shipcloud/latest/actions/create-address', {
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
      "care_of": "string",
      "city": "string",
      "company": "string",
      "country": "string",
      "email": "ava@example.com",
      "first_name": "Ava",
      "id": "string",
      "last_name": "Chen",
      "phone": "string",
      "state": "string",
      "street": "string",
      "street_no": "string",
      "zip_code": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Address action reference](actions/create-address.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/shipcloud/latest/actions/create-address).
