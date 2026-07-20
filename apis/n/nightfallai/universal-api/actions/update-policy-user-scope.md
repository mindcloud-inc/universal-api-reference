# Nightfall.ai: Update Policy User Scope

Updates a policy user scope in Nightfall.ai.

```
PUT https://connect.mindcloud.co/v1/universal/nightfallai/latest/actions/update-policy-user-scope
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nightfall.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/nightfallai/latest/actions/update-policy-user-scope" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "policyID": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nightfallai/latest/actions/update-policy-user-scope', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "policyID": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `policyID` | string | yes | The policy UUID to update. |
| `add` | object | no | Object containing users to add to policy scope. |
| `delete` | object | no | Object containing users to remove from policy scope. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Nightfall.ai API returns.

## Native endpoint

Through the native Nightfall.ai API, this operation is `POST /policy/v1/:policyID/scope/users` (base URL `https://api.nightfall.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-policy-user-scope.md) for the provider-specific parameters and requirements.

