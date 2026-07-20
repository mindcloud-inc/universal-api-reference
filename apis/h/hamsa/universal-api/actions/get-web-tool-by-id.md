# Hamsa: Get a web tool by ID

Retrieves a web tool from Hamsa.

```
GET https://connect.mindcloud.co/v1/universal/hamsa/latest/actions/get-web-tool-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hamsa `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hamsa/latest/actions/get-web-tool-by-id?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hamsa/latest/actions/get-web-tool-by-id?${params}`, {
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
| `id` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "async": true,
      "collectionId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": "string",
      "isActive": true,
      "name": "Ava Chen",
      "persistentId": "string",
      "toolSettings": {
        "methodType": "string",
        "serverUrl": "https://example.com"
      },
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "version": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `async` | boolean |  |
| `collectionId` | string |  |
| `createdAt` | date |  |
| `description` | string |  |
| `id` | string |  |
| `isActive` | boolean |  |
| `name` | string |  |
| `persistentId` | string |  |
| `toolSettings.methodType` | string |  |
| `toolSettings.serverUrl` | string |  |
| `type` | string |  |
| `updatedAt` | date |  |
| `version` | number |  |

## Native endpoint

Through the native Hamsa API, this operation is `GET /v1/voice-agents/web-tool/{id}` (base URL `https://api.tryhamsa.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-web-tool-by-id.md) for the provider-specific parameters and requirements.

