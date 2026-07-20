# Fourthwall Universal API Examples

These examples use the MindCloud API key and Fourthwall connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current Shop

Retrieves the current shop from Fourthwall.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fourthwall/latest/actions/get-current-shop?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fourthwall/latest/actions/get-current-shop?${params}`, {
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
      "domain": "string",
      "id": "string",
      "name": "Ava Chen",
      "publicDomain": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Current Shop action reference](actions/get-current-shop.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/fourthwall/latest/actions/get-current-shop).

## Create Promotion

Creates a new promotion in Fourthwall.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fourthwall/latest/actions/create-promotion" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "type": "MEMBERSHIPS_MULTI",
  "discount": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fourthwall/latest/actions/create-promotion', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "type": "MEMBERSHIPS_MULTI",
    "discount": {}
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
      "appliesTo": {
        "type": "string"
      },
      "code": "string",
      "discount": {
        "percentage": 1,
        "shippingOption": "string",
        "type": "string"
      },
      "id": "string",
      "limits": {
        "maximumUsesNumber": 1,
        "oneUsePerCustomer": true
      },
      "requirements": {
        "minimumOrderValue": 1
      },
      "status": "string",
      "type": "string",
      "usageCount": 1
    }
  ],
  "meta": {}
}
```

See the full [Create Promotion action reference](actions/create-promotion.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/fourthwall/latest/actions/create-promotion).
