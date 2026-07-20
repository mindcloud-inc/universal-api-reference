# Vercel: Update Project Env Var

Updates an existing project environment variable in Vercel.

```
PUT https://connect.mindcloud.co/v1/universal/vercel/latest/actions/update-project-env-var
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vercel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/vercel/latest/actions/update-project-env-var" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "idOrName": "prj_1234567890",
  "id": "env_1234567890"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vercel/latest/actions/update-project-env-var', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "idOrName": "prj_1234567890",
    "id": "env_1234567890"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `idOrName` | string | yes | The unique project identifier or the project name Example: `prj_1234567890`. |
| `id` | string | yes | The unique environment variable identifier Example: `env_1234567890`. |
| `key` | string | no | The name of the environment variable Example: `MINDCLOUD_STAGE3_TOKEN`. |
| `value` | string | no | The value of the environment variable Example: `updated-test-value-123`. |
| `type` | string | no | The type of environment variable Example: `plain`. |
| `target[0]` | string | no | The target environment of the environment variable Example: `preview`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": 1,
      "id": "string",
      "key": "string",
      "target": [
        "string"
      ],
      "type": "string",
      "updatedAt": 1,
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | number | Environment variable creation timestamp |
| `id` | string | The environment variable identifier |
| `key` | string | The environment variable name |
| `target` | array<string> | The target environments for the variable |
| `type` | string | The environment variable type |
| `updatedAt` | number | Environment variable update timestamp |
| `value` | string | The updated environment variable value |

## Native endpoint

Through the native Vercel API, this operation is `PATCH /v9/projects/:idOrName/env/:id` (base URL `https://api.vercel.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-project-env-var.md) for the provider-specific parameters and requirements.

