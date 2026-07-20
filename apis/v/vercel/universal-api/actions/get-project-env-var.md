# Vercel: Get Project Env Var

Retrieves a project environment variable from Vercel.

```
GET https://connect.mindcloud.co/v1/universal/vercel/latest/actions/get-project-env-var
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vercel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vercel/latest/actions/get-project-env-var?connectionId=$CONNECTION_ID&idOrName=prj_1234567890&id=env_1234567890" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "idOrName": "prj_1234567890",
  "id": "env_1234567890"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vercel/latest/actions/get-project-env-var?${params}`, {
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
| `idOrName` | string | yes | The unique project identifier or the project name Example: `prj_1234567890`. |
| `id` | string | yes | The unique environment variable identifier Example: `env_1234567890`. |

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
| `value` | string | The decrypted environment variable value |

## Native endpoint

Through the native Vercel API, this operation is `GET /v1/projects/:idOrName/env/:id` (base URL `https://api.vercel.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project-env-var.md) for the provider-specific parameters and requirements.

