# Explodely: Update Private Affiliate Payout

Updates a private affiliate payout in Explodely.

```
PUT https://connect.mindcloud.co/v1/universal/explodely/latest/actions/update-private-affiliate-payout
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Explodely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/explodely/latest/actions/update-private-affiliate-payout" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "affiliateUsername": "affiliate_username",
  "productId": "allproducts",
  "commission": "25"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/explodely/latest/actions/update-private-affiliate-payout', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "affiliateUsername": "affiliate_username",
    "productId": "allproducts",
    "commission": "25"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `affiliateUsername` | string | yes | The Explodely affiliate username for the private payout. Example: `affiliate_username`. |
| `productId` | string | yes | The Explodely product ID or allproducts. Example: `allproducts`. |
| `commission` | string | yes | The private affiliate commission percentage, from 1 to 80. Example: `25`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "error": "string",
      "private_payout_edited": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `error` | string |  |
| `private_payout_edited` | string |  |

## Native endpoint

Through the native Explodely API, this operation is `POST /aff` (base URL `https://explodely.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-private-affiliate-payout.md) for the provider-specific parameters and requirements.

