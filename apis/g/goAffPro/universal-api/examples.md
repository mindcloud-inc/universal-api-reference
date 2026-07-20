# GoAffPro Universal API Examples

These examples use the MindCloud API key and GoAffPro connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Affiliates

Retrieves a list of affiliates from GoAffPro.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goAffPro/latest/actions/list-affiliates?connectionId=$CONNECTION_ID&limit=25&offset=0&fields%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "fields[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goAffPro/latest/actions/list-affiliates?${params}`, {
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
      "commission": {
        "amount": 1,
        "on": "string",
        "type": "string"
      },
      "country": "string",
      "coupon": "string",
      "coupons": [
        {
          "code": "string",
          "discountType": "string",
          "discountValue": 1
        }
      ],
      "email": "ava@example.com",
      "firstName": "Ava",
      "groupId": 1,
      "id": 1,
      "lastName": "Chen",
      "name": "Ava Chen",
      "paymentMethod": "string",
      "phone": "string",
      "refCode": "string",
      "refCodes": [
        {
          "response": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Affiliates action reference](actions/list-affiliates.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/goAffPro/latest/actions/list-affiliates).

## Create Affiliate

Creates a new affiliate in GoAffPro.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/goAffPro/latest/actions/create-affiliate" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/goAffPro/latest/actions/create-affiliate', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com"
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
      "affiliateId": 1
    }
  ],
  "meta": {}
}
```

See the full [Create Affiliate action reference](actions/create-affiliate.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/goAffPro/latest/actions/create-affiliate).
