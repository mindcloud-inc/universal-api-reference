# ReferralHero: List List Rewards

Retrieves rewards for a list in ReferralHero.

```
GET https://connect.mindcloud.co/v1/universal/referralHero/latest/actions/list-list-rewards
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ReferralHero `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/referralHero/latest/actions/list-list-rewards?connectionId=$CONNECTION_ID&uuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "uuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/referralHero/latest/actions/list-list-rewards?${params}`, {
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
| `uuid` | string | yes | ReferralHero list UUID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "referrals": 1,
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `referrals` | number |  |
| `title` | string |  |

## Native endpoint

Through the native ReferralHero API, this operation is `GET /lists/:uuid/bonuses` (base URL `https://app.referralhero.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-list-rewards.md) for the provider-specific parameters and requirements.

