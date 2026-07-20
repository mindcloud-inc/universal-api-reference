# GoAffPro: Replace Affiliate Referral Codes

Replaces an affiliate's referral codes in GoAffPro.

```
PUT https://connect.mindcloud.co/v1/universal/goAffPro/latest/actions/replace-affiliate-referral-codes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoAffPro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/goAffPro/latest/actions/replace-affiliate-referral-codes" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "referralCodes[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/goAffPro/latest/actions/replace-affiliate-referral-codes', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "referralCodes[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Affiliate ID for the referral codes being replaced. |
| `referralCodes[]` | array<string> | yes | Referral codes to assign to the affiliate. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string | Referral code value |

## Native endpoint

Through the native GoAffPro API, this operation is `PUT /admin/affiliates/:id/referral_codes` (base URL `https://api.goaffpro.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/replace-affiliate-referral-codes.md) for the provider-specific parameters and requirements.

