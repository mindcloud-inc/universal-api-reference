# Xano: Get API Group OpenAPI

Retrieves an OpenAPI specification for a Xano API group.

```
GET https://connect.mindcloud.co/v1/universal/xano/latest/actions/get-api-group-openapi
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Xano `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xano/latest/actions/get-api-group-openapi?connectionId=$CONNECTION_ID&apigroup_id=1&workspace_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "apigroup_id": "1",
  "workspace_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xano/latest/actions/get-api-group-openapi?${params}`, {
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
| `apigroup_id` | number | yes | The Xano API group ID. |
| `workspace_id` | number | yes | The Xano workspace ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "info": {
        "description": "string",
        "title": "string",
        "version": "string"
      },
      "openapi": "string",
      "servers": [
        {
          "url": "https://example.com"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `info.description` | string |  |
| `info.title` | string |  |
| `info.version` | string |  |
| `openapi` | string |  |
| `servers[].url` | string |  |

## Native endpoint

Through the native Xano API, this operation is `GET /api%3Ameta/workspace/:workspace_id/apigroup/:apigroup_id/openapi` (base URL `https://x8ki-letl-twmt.n7.xano.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-api-group-openapi.md) for the provider-specific parameters and requirements.

