# Optimizely: Get Extension

Retrieves extension details from the Optimizely API.

```
GET https://connect.mindcloud.co/v1/universal/optimizely/latest/actions/get-extension
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Optimizely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/optimizely/latest/actions/get-extension?connectionId=$CONNECTION_ID&extensionId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "extensionId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/optimizely/latest/actions/get-extension?${params}`, {
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
| `extensionId` | string | yes | The extension id. Default: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "created": "string",
      "description": "string",
      "editUrl": "https://example.com",
      "enabled": true,
      "id": 1,
      "lastModified": "string",
      "name": "Ava Chen",
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
| `editUrl` | string |  |
| `enabled` | boolean |  |
| `id` | number |  |
| `lastModified` | string |  |
| `name` | string |  |
| `projectId` | number |  |

## Native endpoint

Through the native Optimizely API, this operation is `GET /extensions/{extensionId}` (base URL `https://api.optimizely.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-extension.md) for the provider-specific parameters and requirements.

