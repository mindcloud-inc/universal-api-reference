# v0: Create Environment Variables

Creates project environment variables in v0.

```
POST https://connect.mindcloud.co/v1/universal/v0/latest/actions/create-environment-variables
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a v0 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/v0/latest/actions/create-environment-variables" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "string",
  "environmentVariables[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/v0/latest/actions/create-environment-variables', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "string",
    "environmentVariables[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | string | yes | The ID of the project whose environment variables to create. |
| `environmentVariables[]` | array<object> | yes |  |
| `upsert` | boolean | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `decrypted` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": 1,
      "decrypted": true,
      "id": "string",
      "key": "string",
      "object": "string",
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
| `createdAt` | number |  |
| `decrypted` | boolean |  |
| `id` | string |  |
| `key` | string |  |
| `object` | string |  |
| `updatedAt` | number |  |
| `value` | string |  |

## Native endpoint

Through the native v0 API, this operation is `POST /v1/projects/:projectId/env-vars` (base URL `https://api.v0.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-environment-variables.md) for the provider-specific parameters and requirements.

