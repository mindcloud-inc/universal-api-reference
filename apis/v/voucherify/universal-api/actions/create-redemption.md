# Voucherify: Create Redemption

Creates a redemption in Voucherify.

```
POST https://connect.mindcloud.co/v1/universal/voucherify/latest/actions/create-redemption
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Voucherify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/voucherify/latest/actions/create-redemption" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "orderAmount": 1,
  "redeemables[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/voucherify/latest/actions/create-redemption', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "orderAmount": 1,
    "redeemables[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `orderAmount` | number | yes |  |
| `redeemables[]` | array<object> | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "inapplicableRedeemables": [
        {}
      ],
      "order": {},
      "redemptions": [
        {}
      ],
      "skippedRedeemables": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `inapplicableRedeemables` | array<object> |  |
| `order` | object |  |
| `redemptions` | array<object> |  |
| `skippedRedeemables` | array<object> |  |

## Native endpoint

Through the native Voucherify API, this operation is `POST /redemptions` (base URL `https://us1.api.voucherify.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-redemption.md) for the provider-specific parameters and requirements.

