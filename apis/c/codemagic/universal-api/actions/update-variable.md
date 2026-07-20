# Codemagic: Update Variable

Updates an existing variable in a Codemagic group.

```
PUT https://connect.mindcloud.co/v1/universal/codemagic/latest/actions/update-variable
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Codemagic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/codemagic/latest/actions/update-variable" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "variableGroupId": "string",
  "variableId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/codemagic/latest/actions/update-variable', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "variableGroupId": "string",
    "variableId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `variableGroupId` | string | yes | Codemagic variable group identifier. |
| `variableId` | string | yes | Codemagic environment variable identifier. |
| `name` | string | no | Optional new variable name. |
| `value` | string | no | Optional new variable value. |
| `secure` | boolean | no | Whether the variable should be stored securely. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Codemagic API returns.

## Native endpoint

Through the native Codemagic API, this operation is `PATCH /api/v3/variable-groups/:variable_group_id/variables/:variable_id` (base URL `https://codemagic.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-variable.md) for the provider-specific parameters and requirements.

