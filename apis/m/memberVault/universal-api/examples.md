# MemberVault Universal API Examples

These examples use the MindCloud API key and MemberVault connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Products

Retrieves products from your MemberVault account.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/memberVault/latest/actions/list-products?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/memberVault/latest/actions/list-products?${params}`, {
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
      "id": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Products action reference](actions/list-products.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/memberVault/latest/actions/list-products).

## Add User to Product

Adds a user to a MemberVault product, creating them if needed.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/memberVault/latest/actions/add-user-to-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "courseKey": "string",
  "email": "ava@example.com",
  "firstName": "Ava",
  "lastName": "Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/memberVault/latest/actions/add-user-to-product', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "courseKey": "string",
    "email": "ava@example.com",
    "firstName": "Ava",
    "lastName": "Chen"
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
      "userId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add User to Product action reference](actions/add-user-to-product.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/memberVault/latest/actions/add-user-to-product).
