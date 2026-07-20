# ReferralHero: List Level 1 Referrals

Retrieves level 1 referrals from ReferralHero.

```
GET https://connect.mindcloud.co/v1/universal/referralHero/latest/actions/list-level1-referrals
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ReferralHero `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/referralHero/latest/actions/list-level1-referrals?connectionId=$CONNECTION_ID&subscriberId=string&uuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "subscriberId": "string",
  "uuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/referralHero/latest/actions/list-level1-referrals?${params}`, {
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
| `subscriberId` | string | yes | Subscriber ID. |
| `uuid` | string | yes | ReferralHero list UUID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "createdAt": 1,
      "email": "ava@example.com",
      "id": "string",
      "lastUpdatedAt": 1,
      "name": "Ava Chen",
      "response": "string",
      "universalLink": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string |  |
| `createdAt` | number |  |
| `email` | string |  |
| `id` | string |  |
| `lastUpdatedAt` | number |  |
| `name` | string |  |
| `response` | string |  |
| `universalLink` | string |  |

## Native endpoint

Through the native ReferralHero API, this operation is `GET /lists/:uuid/subscribers/:subscriber_id/level_1_referrals` (base URL `https://app.referralhero.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-level1-referrals.md) for the provider-specific parameters and requirements.

