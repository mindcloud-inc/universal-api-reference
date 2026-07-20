# Vercel: Create Project Env Vars

Creates project environment variables in Vercel.

```
POST https://connect.mindcloud.co/v1/universal/vercel/latest/actions/create-project-env-vars
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vercel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/vercel/latest/actions/create-project-env-vars" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "idOrName": "prj_1234567890",
  "key": "MINDCLOUD_STAGE3_TOKEN",
  "value": "test-value-123",
  "type": "plain",
  "target[0]": "preview"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vercel/latest/actions/create-project-env-vars', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "idOrName": "prj_1234567890",
    "key": "MINDCLOUD_STAGE3_TOKEN",
    "value": "test-value-123",
    "type": "plain",
    "target[0]": "preview"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `idOrName` | string | yes | The unique project identifier or the project name Example: `prj_1234567890`. |
| `key` | string | yes | The name of the environment variable Example: `MINDCLOUD_STAGE3_TOKEN`. |
| `value` | string | yes | The value of the environment variable Example: `test-value-123`. |
| `type` | string | yes | The type of environment variable Example: `plain`. |
| `target[0]` | string | yes | The target environment of the environment variable Example: `preview`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": {},
      "failed": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | object | The environment variable that was created |
| `failed` | array<object> | Any environment variables that failed to be created |

## Native endpoint

Through the native Vercel API, this operation is `POST /v10/projects/:idOrName/env` (base URL `https://api.vercel.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-project-env-vars.md) for the provider-specific parameters and requirements.

