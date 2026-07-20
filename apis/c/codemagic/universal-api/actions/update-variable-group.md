# Codemagic: Update Variable Group

Updates an existing variable group in Codemagic.

```
PUT https://connect.mindcloud.co/v1/universal/codemagic/latest/actions/update-variable-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Codemagic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/codemagic/latest/actions/update-variable-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "variableGroupId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/codemagic/latest/actions/update-variable-group', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "variableGroupId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `variableGroupId` | string | yes | Codemagic variable group identifier. |
| `name` | string | no | Optional new variable group name. |
| `advancedSecurity` | object | no | Optional advanced security object for team variable groups. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Codemagic API returns.

## Native endpoint

Through the native Codemagic API, this operation is `PATCH /api/v3/variable-groups/:variable_group_id` (base URL `https://codemagic.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-variable-group.md) for the provider-specific parameters and requirements.

