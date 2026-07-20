# Cinode Universal API Examples

These examples use the MindCloud API key and Cinode connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current User

Retrieves the current user identity from Cinode.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cinode/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cinode/latest/actions/get-current-user?${params}`, {
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
      "companyId": 1,
      "companyUserId": 1
    }
  ],
  "meta": {}
}
```

See the full [Get Current User action reference](actions/get-current-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/cinode/latest/actions/get-current-user).

## Add Customer Tag

Adds a tag to a customer in Cinode.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cinode/latest/actions/add-customer-tag" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "companyId": 1,
  "customerId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cinode/latest/actions/add-customer-tag', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "companyId": 1,
    "customerId": 1
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
      "companyId": 1,
      "id": 1,
      "name": "Ava Chen",
      "seoId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Customer Tag action reference](actions/add-customer-tag.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/cinode/latest/actions/add-customer-tag).
