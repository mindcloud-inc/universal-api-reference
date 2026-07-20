# InviteReferrals: Add Conversion



```
POST https://connect.mindcloud.co/v1/universal/inviteReferrals/latest/actions/add-conversion
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a InviteReferrals `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/inviteReferrals/latest/actions/add-conversion" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "orderId": "string",
  "campaignId": 1,
  "refereeName": "Ava Chen",
  "refereeEmail": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/inviteReferrals/latest/actions/add-conversion', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "orderId": "string",
    "campaignId": 1,
    "refereeName": "Ava Chen",
    "refereeEmail": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `orderId` | string | yes | Unique order identifier for the conversion. |
| `campaignId` | number | yes | InviteReferrals campaign identifier. |
| `refereeName` | string | yes | Name of the referred customer tied to the conversion. |
| `refereeEmail` | string | yes | Email address of the referred customer tied to the conversion. |
| `referrerCode` | string | no | Referral code given by the referrer to the customer to attribute the conversion. |
| `uniqueCode` | string | no | Unique code sent by the referrer to the customer to attribute the conversion. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `status` | number |  |

## Native endpoint

Through the native InviteReferrals API, this operation is `POST /conversion/add` (base URL `https://www.ref-r.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-conversion.md) for the provider-specific parameters and requirements.

