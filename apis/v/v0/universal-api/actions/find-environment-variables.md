# v0: Find Environment Variables

Finds project environment variables in v0.

```
GET https://connect.mindcloud.co/v1/universal/v0/latest/actions/find-environment-variables
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a v0 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/v0/latest/actions/find-environment-variables?connectionId=$CONNECTION_ID&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/v0/latest/actions/find-environment-variables?${params}`, {
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
| `projectId` | string | yes | The ID of the project whose environment variables to list. |

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

Through the native v0 API, this operation is `GET /v1/projects/:projectId/env-vars` (base URL `https://api.v0.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-environment-variables.md) for the provider-specific parameters and requirements.

