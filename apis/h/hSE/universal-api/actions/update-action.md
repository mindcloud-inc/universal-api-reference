# 4HSE: Update Action

Updates an existing action in 4HSE.

```
PUT https://connect.mindcloud.co/v1/universal/hSE/latest/actions/update-action
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 4HSE `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/hSE/latest/actions/update-action" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "a2f09656-150b-4fc2-a79f-1267260d1d36",
  "name": "Updated action name"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hSE/latest/actions/update-action', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "a2f09656-150b-4fc2-a79f-1267260d1d36",
    "name": "Updated action name"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The action_id to update. Example: `a2f09656-150b-4fc2-a79f-1267260d1d36`. |
| `name` | string | yes | Descriptive name of the action. Example: `Updated action name`. |
| `validity` | number | no | Number of validity units. Example: `5`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native 4HSE API returns.

## Native endpoint

Through the native 4HSE API, this operation is `PUT /v2/action/update/:id` (base URL `https://service.4hse.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-action.md) for the provider-specific parameters and requirements.

