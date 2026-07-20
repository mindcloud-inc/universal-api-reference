# Soundee Universal API Examples

These examples use the MindCloud API key and Soundee connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Account

Retrieves your Soundee producer account details.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/soundee/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/soundee/latest/actions/get-account?${params}`, {
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
      "active": 1,
      "admin": 1,
      "avatar": {},
      "bio": "string",
      "color": "string",
      "country": {},
      "countryId": 1,
      "created": 1,
      "displayname": "Ava Chen",
      "email": "ava@example.com",
      "entityId": 1,
      "firstName": "Ava",
      "id": 1,
      "interaction": {},
      "isProducer": 1,
      "lastName": "Chen",
      "socials": [
        {}
      ],
      "subscription": {},
      "type": "string",
      "uploads": 1,
      "username": "Ava Chen",
      "vatNumber": "string",
      "verified": 1
    }
  ],
  "meta": {}
}
```

See the full [Get Account action reference](actions/get-account.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/soundee/latest/actions/get-account).

## Create Coupon

Creates a new coupon in Soundee.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/soundee/latest/actions/create-coupon" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/soundee/latest/actions/create-coupon', {
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
      "active": 1,
      "amount": 1,
      "amount_off_string": "string",
      "conditions": {},
      "created": 1,
      "endDate": 1,
      "exclusives": 1,
      "id": 1,
      "maxUsage": 1,
      "minCartAmount": 1,
      "minCartItems": 1,
      "name": "Ava Chen",
      "neverEnd": 1,
      "startDate": 1,
      "stopBulkDiscounts": 1,
      "type": "string",
      "upgrades": 1,
      "used": 1,
      "userId": 1
    }
  ],
  "meta": {}
}
```

See the full [Create Coupon action reference](actions/create-coupon.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/soundee/latest/actions/create-coupon).
