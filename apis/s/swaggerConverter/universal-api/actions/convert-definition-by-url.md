# Swagger Converter: Convert Definition by URL

Retrieves a converted OpenAPI document from Swagger Converter by source URL.

```
GET https://connect.mindcloud.co/v1/universal/swaggerConverter/latest/actions/convert-definition-by-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Swagger Converter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/swaggerConverter/latest/actions/convert-definition-by-url?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fpetstore.swagger.io%2Fv2%2Fswagger.json" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://petstore.swagger.io/v2/swagger.json"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/swaggerConverter/latest/actions/convert-definition-by-url?${params}`, {
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
| `url` | string | yes | A URL to the Swagger/OpenAPI 1.x or 2.x definition to convert. Example: `https://petstore.swagger.io/v2/swagger.json`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Swagger Converter API returns.

## Native endpoint

Through the native Swagger Converter API, this operation is `GET convert` (base URL `https://converter.swagger.io/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/convert-definition-by-url.md) for the provider-specific parameters and requirements.

