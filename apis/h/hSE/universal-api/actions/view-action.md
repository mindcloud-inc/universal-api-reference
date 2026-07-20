# 4HSE: View Action

Retrieves an action from 4HSE.

```
GET https://connect.mindcloud.co/v1/universal/hSE/latest/actions/view-action
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 4HSE `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hSE/latest/actions/view-action?connectionId=$CONNECTION_ID&id=a2f09656-150b-4fc2-a79f-1267260d1d36" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "a2f09656-150b-4fc2-a79f-1267260d1d36"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hSE/latest/actions/view-action?${params}`, {
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
| `id` | string | yes | The action_id to view. Example: `a2f09656-150b-4fc2-a79f-1267260d1d36`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native 4HSE API returns.

## Native endpoint

Through the native 4HSE API, this operation is `GET /v2/action/view/:id` (base URL `https://service.4hse.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/view-action.md) for the provider-specific parameters and requirements.

