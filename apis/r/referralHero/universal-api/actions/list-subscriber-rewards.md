# ReferralHero: List Subscriber Rewards

Retrieves rewards unlocked by a subscriber in ReferralHero.

```
GET https://connect.mindcloud.co/v1/universal/referralHero/latest/actions/list-subscriber-rewards
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ReferralHero `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/referralHero/latest/actions/list-subscriber-rewards?connectionId=$CONNECTION_ID&subscriberId=string&uuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "subscriberId": "string",
  "uuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/referralHero/latest/actions/list-subscriber-rewards?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `status` | string | no | Optional reward status filter. |
| `subscriberId` | string | yes | Subscriber ID. |
| `uuid` | string | yes | ReferralHero list UUID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "couponCode": "string",
      "couponGroup": "string",
      "createdAt": 1,
      "id": 1,
      "imageUrl": "https://example.com",
      "name": "Ava Chen",
      "recurringCount": 1,
      "referral": "string",
      "referrals": 1,
      "referralsType": "string",
      "sentDate": 1,
      "signupType": "string",
      "status": "string",
      "total": "string",
      "unlockedDate": 1,
      "value": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `couponCode` | string |  |
| `couponGroup` | string |  |
| `createdAt` | number |  |
| `id` | number |  |
| `imageUrl` | string |  |
| `name` | string |  |
| `recurringCount` | number |  |
| `referral` | string |  |
| `referrals` | number |  |
| `referralsType` | string |  |
| `sentDate` | number |  |
| `signupType` | string |  |
| `status` | string |  |
| `total` | string |  |
| `unlockedDate` | number |  |
| `value` | number |  |

## Native endpoint

Through the native ReferralHero API, this operation is `GET /lists/:uuid/subscribers/:subscriber_id/rewards` (base URL `https://app.referralhero.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-subscriber-rewards.md) for the provider-specific parameters and requirements.

