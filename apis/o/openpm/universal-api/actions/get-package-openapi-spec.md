# openpm: Get Package OpenAPI Spec



```
GET https://connect.mindcloud.co/v1/universal/openpm/latest/actions/get-package-openapi-spec
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a openpm `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openpm/latest/actions/get-package-openapi-spec?connectionId=$CONNECTION_ID&packageId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "packageId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openpm/latest/actions/get-package-openapi-spec?${params}`, {
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
| `packageId` | string | yes | Package ID. |
| `format` | list | no | OpenAPI spec format. Supported values are json and yaml. One of: `0`, `1`. Default: `json`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "components": {},
      "info": {},
      "openapi": "string",
      "paths": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `components` | object | OpenAPI components object. |
| `info` | object | OpenAPI info object. |
| `openapi` | string | OpenAPI version string. |
| `paths` | object | OpenAPI paths object. |

## Native endpoint

Through the native openpm API, this operation is `GET /packages/:packageId/openapi` (base URL `https://openpm.ai/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-package-openapi-spec.md) for the provider-specific parameters and requirements.

