# Payhip Universal API Examples

These examples use the MindCloud API key and Payhip connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Coupons

Retrieves a paginated list of coupons from Payhip.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/payhip/latest/actions/list-coupons?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/payhip/latest/actions/list-coupons?${params}`, {
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
      "amountOff": 1,
      "code": "string",
      "collectionId": "string",
      "couponType": "string",
      "endDate": "string",
      "id": "string",
      "minimumPurchaseAmount": 1,
      "notes": "string",
      "percentOff": 1,
      "productKey": "string",
      "startDate": "string",
      "usageLimit": 1
    }
  ],
  "meta": {}
}
```

See the full [List Coupons action reference](actions/list-coupons.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/payhip/latest/actions/list-coupons).

## Create Coupon

Creates a new coupon in Payhip.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/payhip/latest/actions/create-coupon" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "couponType": "all_products",
  "code": "SPRING2026"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/payhip/latest/actions/create-coupon', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "couponType": "all_products",
    "code": "SPRING2026"
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
      "amountOff": 1,
      "code": "string",
      "collectionId": "string",
      "couponType": "string",
      "endDate": "string",
      "id": "string",
      "minimumPurchaseAmount": 1,
      "notes": "string",
      "percentOff": 1,
      "productKey": "string",
      "startDate": "string",
      "usageLimit": 1
    }
  ],
  "meta": {}
}
```

See the full [Create Coupon action reference](actions/create-coupon.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/payhip/latest/actions/create-coupon).
