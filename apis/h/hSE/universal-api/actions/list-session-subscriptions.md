# 4HSE: List Session Subscriptions

Retrieves session subscriptions from 4HSE.

```
GET https://connect.mindcloud.co/v1/universal/hSE/latest/actions/list-session-subscriptions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 4HSE `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hSE/latest/actions/list-session-subscriptions?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hSE/latest/actions/list-session-subscriptions?${params}`, {
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
      "actionSessionId": "string",
      "actionSessionSubscriptionId": "string",
      "actionSubscriptionId": "string",
      "certificateId": "string",
      "dateBegin": "2026-05-07T12:00:00.000Z",
      "dateExpire": "2026-05-07T12:00:00.000Z",
      "done": 1,
      "permission": "string",
      "subscriberId": "string",
      "subscriberName": "Ava Chen",
      "subscriberType": "string",
      "warning": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actionSessionId` | string | Action session identifier |
| `actionSessionSubscriptionId` | string | Action session subscription identifier |
| `actionSubscriptionId` | string | Action subscription identifier |
| `certificateId` | string | Certificate identifier |
| `dateBegin` | date | Start date |
| `dateExpire` | date | Expiry date |
| `done` | number | Completion flag |
| `permission` | string | Permission level |
| `subscriberId` | string | Subscribed resource identifier |
| `subscriberName` | string | Subscribed resource name |
| `subscriberType` | string | Subscribed resource type |
| `warning` | number | Warning flag |

## Native endpoint

Through the native 4HSE API, this operation is `POST /v2/action-session-subscription/index` (base URL `https://service.4hse.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-session-subscriptions.md) for the provider-specific parameters and requirements.

