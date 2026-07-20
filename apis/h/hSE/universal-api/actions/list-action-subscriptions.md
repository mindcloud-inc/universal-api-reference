# 4HSE: List Action Subscriptions

Retrieves action subscriptions from 4HSE.

```
GET https://connect.mindcloud.co/v1/universal/hSE/latest/actions/list-action-subscriptions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 4HSE `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hSE/latest/actions/list-action-subscriptions?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hSE/latest/actions/list-action-subscriptions?${params}`, {
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
| `filter.actionId` | string | no | Filter by preventive action. |
| `filter.actionType` | string | no | Filter by action type. One of: `0`, `1`, `2`, `3`, `4`. |
| `filter.subscriberId` | string | no | Filter by subscribed resource. |
| `filter.status` | string | no | Filter by compliance status. One of: `0`, `1`, `2`, `3`. |
| `filter.subtenantId` | string | no | Filter by office. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `filter.actionSubscriptionId` | string | no | Filter by compliance schedule entry ID. |
| `filter.subscriberType` | string | no | Filter by subscribed resource type. One of: `0`, `1`, `2`, `3`, `4`, `5`, `6`, `7`, `8`. |
| `filter.tenantId` | string | no | Filter by project. |
| `history` | boolean | no | Include historicized entries in the results. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "actionId": "string",
      "actionName": "Ava Chen",
      "actionSubscriptionId": "string",
      "actionType": "string",
      "officeName": "Ava Chen",
      "permission": "string",
      "status": "string",
      "subscriberId": "string",
      "subscriberName": "Ava Chen",
      "subscriberType": "string",
      "subtenantId": "string",
      "tenantId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actionId` | string | Action identifier |
| `actionName` | string | Action name |
| `actionSubscriptionId` | string | Action subscription identifier |
| `actionType` | string | Action type |
| `officeName` | string | Office name |
| `permission` | string | Permission level |
| `status` | string | Subscription status |
| `subscriberId` | string | Subscribed resource identifier |
| `subscriberName` | string | Subscribed resource name |
| `subscriberType` | string | Subscribed resource type |
| `subtenantId` | string | Office identifier |
| `tenantId` | string | Project identifier |

## Native endpoint

Through the native 4HSE API, this operation is `POST /v2/action-subscription/index` (base URL `https://service.4hse.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-action-subscriptions.md) for the provider-specific parameters and requirements.

