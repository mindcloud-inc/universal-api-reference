# CircleCI: Upsert Context Environment Variable



```
PUT https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/upsert-context-environment-variable
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CircleCI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/upsert-context-environment-variable" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "value": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/upsert-context-environment-variable', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "value": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `context_id` | string | no | The CircleCI context UUID. |
| `env_var_name` | string | no | The environment variable name. |
| `value` | string | yes | The environment variable value. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contextId": "string",
      "createdAt": "string",
      "message": "string",
      "updatedAt": "string",
      "variable": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contextId` | string |  |
| `createdAt` | string |  |
| `message` | string |  |
| `updatedAt` | string |  |
| `variable` | string |  |

## Native endpoint

Through the native CircleCI API, this operation is `PUT /context/:context_id/environment-variable/:env_var_name` (base URL `https://circleci.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upsert-context-environment-variable.md) for the provider-specific parameters and requirements.

