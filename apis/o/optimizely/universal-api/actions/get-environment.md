# Optimizely: Get Environment

Retrieves environment details from the Optimizely API.

```
GET https://connect.mindcloud.co/v1/universal/optimizely/latest/actions/get-environment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Optimizely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/optimizely/latest/actions/get-environment?connectionId=$CONNECTION_ID&environmentId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "environmentId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/optimizely/latest/actions/get-environment?${params}`, {
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
| `environmentId` | string | yes | The environment id. Default: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "created": "string",
      "description": "string",
      "hasRestrictedPermissions": true,
      "id": 1,
      "isPrimary": true,
      "key": "string",
      "lastModified": "string",
      "name": "Ava Chen",
      "priority": 1,
      "projectId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean |  |
| `created` | string |  |
| `description` | string |  |
| `hasRestrictedPermissions` | boolean |  |
| `id` | number |  |
| `isPrimary` | boolean |  |
| `key` | string |  |
| `lastModified` | string |  |
| `name` | string |  |
| `priority` | number |  |
| `projectId` | number |  |

## Native endpoint

Through the native Optimizely API, this operation is `GET /environments/{environmentId}` (base URL `https://api.optimizely.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-environment.md) for the provider-specific parameters and requirements.

