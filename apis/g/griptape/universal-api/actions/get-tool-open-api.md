# Griptape: Get Tool OpenAPI

Retrieves a tool OpenAPI schema from Griptape.

```
GET https://connect.mindcloud.co/v1/universal/griptape/latest/actions/get-tool-open-api
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Griptape `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/griptape/latest/actions/get-tool-open-api?connectionId=$CONNECTION_ID&toolId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "toolId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/griptape/latest/actions/get-tool-open-api?${params}`, {
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
| `toolId` | string | yes | The Griptape tool ID whose OpenAPI definition should be retrieved. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "components": {},
      "info": {
        "title": "string",
        "version": "string"
      },
      "openapi": "string",
      "paths": {},
      "servers": [
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
| `components` | object | OpenAPI components object, including request and response schemas when present. |
| `info.title` | string | Tool title from the OpenAPI document. |
| `info.version` | string | Tool version from the OpenAPI document. |
| `openapi` | string | OpenAPI specification version string published by the tool. |
| `paths` | object | OpenAPI paths object containing the tool's available activities. |
| `servers` | array<object> | Server definitions published by the tool's OpenAPI document. |

## Native endpoint

Through the native Griptape API, this operation is `GET /api/tools/:tool_id/openapi` (base URL `https://cloud.griptape.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-tool-open-api.md) for the provider-specific parameters and requirements.

