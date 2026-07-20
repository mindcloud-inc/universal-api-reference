# 4HSE: Create Session Subscription

Creates a new session subscription in 4HSE.

```
POST https://connect.mindcloud.co/v1/universal/hSE/latest/actions/create-session-subscription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 4HSE `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hSE/latest/actions/create-session-subscription" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "actionSessionId": "string",
  "actionSubscriptionId": "string",
  "subtenantId": "string",
  "tenantId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hSE/latest/actions/create-session-subscription', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "actionSessionId": "string",
    "actionSubscriptionId": "string",
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
| `actionSessionId` | string | yes | The session the resource is enrolled in. |
| `actionSubscriptionId` | string | yes | The compliance schedule entry linked to this enrollment. |
| `subtenantId` | string | yes | The office of this enrollment. |
| `tenantId` | string | yes | The project of this enrollment. |
| `done` | number | no | Session outcome for this enrollee. One of: `0`, `1`, `2`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data` | object | no | Additional structured data in JSON format. |
| `warning` | number | no | Warning flag for this enrollment. One of: `0`, `1`. |
| `certificateId` | string | no | Certificate generated from this session for this enrollee. |
| `dateBegin` | date | no | Start date of validity for this enrollment. |
| `dateExpire` | date | no | Expiration date for this enrollment. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native 4HSE API returns.

## Native endpoint

Through the native 4HSE API, this operation is `POST /v2/action-session-subscription/create` (base URL `https://service.4hse.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-session-subscription.md) for the provider-specific parameters and requirements.

