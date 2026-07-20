# Easymailing: Get My Subscription

Retrieves your subscription from Easymailing.

```
GET https://connect.mindcloud.co/v1/universal/easymailing/latest/actions/get-my-subscription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Easymailing `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/easymailing/latest/actions/get-my-subscription?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/easymailing/latest/actions/get-my-subscription?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "aiCostLimitCents": 1,
      "aiCostUsedCents": 1,
      "aiOverageLimitCents": {},
      "allowAiOverage": true,
      "audiences": 1,
      "automations": 1,
      "automationTriggers": 1,
      "canHaveAiOverage": true,
      "credits": 1,
      "creditsUsed": 1,
      "domain": "string",
      "expirationDate": "2026-05-07T12:00:00.000Z",
      "locale": "string",
      "maxSubscribers": 1,
      "subscribersUsed": 1,
      "tier": "string",
      "user": {
        "email": "ava@example.com",
        "firstname": "Ava",
        "lastname": {},
        "role": "string",
        "timezone": "string"
      },
      "websites": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `aiCostLimitCents` | number |  |
| `aiCostUsedCents` | number |  |
| `aiOverageLimitCents` | object |  |
| `allowAiOverage` | boolean |  |
| `audiences` | number |  |
| `automations` | number |  |
| `automationTriggers` | number |  |
| `canHaveAiOverage` | boolean |  |
| `credits` | number |  |
| `creditsUsed` | number |  |
| `domain` | string |  |
| `expirationDate` | date |  |
| `locale` | string |  |
| `maxSubscribers` | number |  |
| `subscribersUsed` | number |  |
| `tier` | string |  |
| `user.email` | string |  |
| `user.firstname` | string |  |
| `user.lastname` | object |  |
| `user.role` | string |  |
| `user.timezone` | string |  |
| `websites` | number |  |

## Native endpoint

Through the native Easymailing API, this operation is `GET /my_suscription` (base URL `https://api.easymailing.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-my-subscription.md) for the provider-specific parameters and requirements.

