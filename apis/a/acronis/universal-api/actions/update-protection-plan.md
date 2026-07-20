# Acronis: Update Protection Plan

Updates an existing protection plan in Acronis.

```
PUT https://connect.mindcloud.co/v1/universal/acronis/latest/actions/update-protection-plan
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Acronis `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/acronis/latest/actions/update-protection-plan" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "policyId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/acronis/latest/actions/update-protection-plan', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "policyId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `policyId` | string | yes | Policy Id path parameter. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Acronis API returns.

## Native endpoint

Through the native Acronis API, this operation is `PATCH /api/policy_management/v4/policies/{policy_id}` (base URL `{{credentials.dataCenterUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-protection-plan.md) for the provider-specific parameters and requirements.

