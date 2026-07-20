# OnePlan: Get My Work Tasks

Retrieves My Work tasks from OnePlan.

```
GET https://connect.mindcloud.co/v1/universal/onePlan/latest/actions/get-my-work-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OnePlan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/onePlan/latest/actions/get-my-work-tasks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/onePlan/latest/actions/get-my-work-tasks?${params}`, {
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
| `PeriodEnd` | string | no | Optional period end date from the docs. |
| `PeriodStart` | string | no | Optional period start date from the docs. |
| `ShowComplete` | string | no | Optional flag to include completed work. |
| `UserId` | string | no | Optional user identifier filter. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native OnePlan API returns.

## Native endpoint

Through the native OnePlan API, this operation is `GET /mywork/tasks` (base URL `https://my.oneplan.ai/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-my-work-tasks.md) for the provider-specific parameters and requirements.

