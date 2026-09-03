# Stripe: Retrieve Subscription Schedule



```
GET https://connect.mindcloud.co/v1/universal/stripe/latest/actions/retrieve-subscription-schedule
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stripe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stripe/latest/actions/retrieve-subscription-schedule?connectionId=$CONNECTION_ID&schedule=sub_sched_..." \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "schedule": "sub_sched_..."
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stripe/latest/actions/retrieve-subscription-schedule?${params}`, {
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
| `schedule` | string | yes | Example: `sub_sched_...`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "canceledAt": 1,
      "completedAt": 1,
      "created": 1,
      "currentPhase": {},
      "customer": "string",
      "endBehavior": "string",
      "id": "string",
      "phases": [
        {}
      ],
      "releasedAt": 1,
      "status": "string",
      "subscription": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `canceledAt` | number |  |
| `completedAt` | number |  |
| `created` | number |  |
| `currentPhase` | object |  |
| `customer` | string |  |
| `endBehavior` | string |  |
| `id` | string |  |
| `phases` | array<object> |  |
| `releasedAt` | number |  |
| `status` | string |  |
| `subscription` | string |  |

## Native endpoint

Through the native Stripe API, this operation is `GET subscription_schedules/:schedule` (base URL `https://api.stripe.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-subscription-schedule.md) for the provider-specific parameters and requirements.

