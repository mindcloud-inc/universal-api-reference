# Whisky Hunter: Get API Schema

Retrieves the Whisky Hunter API schema.

```
GET https://connect.mindcloud.co/v1/universal/whiskyHunter/latest/actions/get-api-schema
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Whisky Hunter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/whiskyHunter/latest/actions/get-api-schema?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/whiskyHunter/latest/actions/get-api-schema?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "basePath": "string",
      "consumes": [
        "string"
      ],
      "definitions": {},
      "host": "string",
      "info": {},
      "paths": {},
      "produces": [
        "string"
      ],
      "schemes": [
        "string"
      ],
      "security": [
        {}
      ],
      "securityDefinitions": {},
      "swagger": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `basePath` | string | API base path. |
| `consumes` | array<string> | Accepted request content types. |
| `definitions` | object | Schema definitions declared by the API. |
| `host` | string | API host. |
| `info` | object | API title, description, and version metadata. |
| `paths` | object | Documented API endpoint paths and methods. |
| `produces` | array<string> | Response content types. |
| `schemes` | array<string> | Supported URL schemes. |
| `security` | array<object> | Global security metadata from the API schema. |
| `securityDefinitions` | object | Authentication scheme metadata from the API schema. |
| `swagger` | string | Swagger specification version. |

## Native endpoint

Through the native Whisky Hunter API, this operation is `GET /` (base URL `https://whiskyhunter.net/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-api-schema.md) for the provider-specific parameters and requirements.

