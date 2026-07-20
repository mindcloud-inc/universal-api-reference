# 4HSE: Create Action Subscription

Creates a new action subscription in 4HSE.

```
POST https://connect.mindcloud.co/v1/universal/hSE/latest/actions/create-action-subscription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 4HSE `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hSE/latest/actions/create-action-subscription" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "actionId": "string",
  "subscriberId": "string",
  "subscriberType": "0",
  "subtenantId": "string",
  "tenantId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hSE/latest/actions/create-action-subscription', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "actionId": "string",
    "subscriberId": "string",
    "subscriberType": "0",
    "subtenantId": "string",
    "tenantId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `actionId` | string | yes | The preventive action this resource is subscribed to. |
| `subscriberId` | string | yes | The ID of the subscribed resource. |
| `subscriberType` | string | yes | The type of subscribed resource. One of: `0`, `1`, `2`, `3`, `4`, `5`, `6`, `7`, `8`. |
| `subtenantId` | string | yes | The office of this subscription. |
| `tenantId` | string | yes | The project of this subscription. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data` | object | no | Additional structured data in JSON format. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native 4HSE API returns.

## Native endpoint

Through the native 4HSE API, this operation is `POST /v2/action-subscription/create` (base URL `https://service.4hse.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-action-subscription.md) for the provider-specific parameters and requirements.

