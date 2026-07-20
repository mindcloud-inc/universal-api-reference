# Codemagic: Bulk Import Variables For Group

Bulk imports variables into a Codemagic variable group.

```
POST https://connect.mindcloud.co/v1/universal/codemagic/latest/actions/bulk-import-variables-for-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Codemagic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/codemagic/latest/actions/bulk-import-variables-for-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "variableGroupId": "string",
  "secure": true,
  "variables[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/codemagic/latest/actions/bulk-import-variables-for-group', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "variableGroupId": "string",
    "secure": true,
    "variables[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `variableGroupId` | string | yes | Codemagic variable group identifier. |
| `secure` | boolean | yes | Whether imported variables should be stored securely. |
| `variables[]` | array<object> | yes | Variables to import. Each item includes name and value. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Codemagic API returns.

## Native endpoint

Through the native Codemagic API, this operation is `POST /api/v3/variable-groups/:variable_group_id/variables` (base URL `https://codemagic.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/bulk-import-variables-for-group.md) for the provider-specific parameters and requirements.

