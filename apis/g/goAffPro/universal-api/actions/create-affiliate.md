# GoAffPro: Create Affiliate

Creates a new affiliate in GoAffPro.

```
POST https://connect.mindcloud.co/v1/universal/goAffPro/latest/actions/create-affiliate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoAffPro `connectionId` ([setup](../authentication.md)).

## Example request

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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | Affiliate email address. |
| `name` | string | no | Affiliate display name. |
| `refCode` | string | no | Referral code for the affiliate. |
| `status` | string | no | Affiliate approval status. |

## Response

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

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `affiliateId` | number | Created affiliate ID |

## Native endpoint

Through the native GoAffPro API, this operation is `POST /admin/affiliates` (base URL `https://api.goaffpro.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-affiliate.md) for the provider-specific parameters and requirements.

