# OnePlan: Get Work Types For Plan

Retrieves work types for a plan from OnePlan.

```
GET https://connect.mindcloud.co/v1/universal/onePlan/latest/actions/get-work-types-for-plan
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OnePlan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/onePlan/latest/actions/get-work-types-for-plan?connectionId=$CONNECTION_ID&PlanId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "PlanId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/onePlan/latest/actions/get-work-types-for-plan?${params}`, {
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
| `PlanId` | string | yes | Plan identifier from the path. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native OnePlan API returns.

## Native endpoint

Through the native OnePlan API, this operation is `GET /workplan/{PlanId}/worktypes` (base URL `https://my.oneplan.ai/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-work-types-for-plan.md) for the provider-specific parameters and requirements.

