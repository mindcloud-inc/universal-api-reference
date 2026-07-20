# Fiserv Universal API Examples

These examples use the MindCloud API key and Fiserv connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Banking Hub Access Token

Retrieves a Banking Hub access token from Fiserv.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fiserv/latest/actions/get-banking-hub-access-token?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fiserv/latest/actions/get-banking-hub-access-token?${params}`, {
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
      "accessToken": "string",
      "expiresIn": "string",
      "tokenType": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Banking Hub Access Token action reference](actions/get-banking-hub-access-token.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/fiserv/latest/actions/get-banking-hub-access-token).

## Calculate Surcharge

Calculates a surcharge for a payment in Fiserv.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fiserv/latest/actions/calculate-surcharge" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "xAccountId": "string",
  "paymentMethodId": "string",
  "amount": 1,
  "percent": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fiserv/latest/actions/calculate-surcharge', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "xAccountId": "string",
    "paymentMethodId": "string",
    "amount": 1,
    "percent": 1
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [],
  "meta": {}
}
```

See the full [Calculate Surcharge action reference](actions/calculate-surcharge.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/fiserv/latest/actions/calculate-surcharge).
