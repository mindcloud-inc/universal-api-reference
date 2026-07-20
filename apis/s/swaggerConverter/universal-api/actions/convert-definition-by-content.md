# Swagger Converter: Convert Definition by Content

Creates a converted OpenAPI document in Swagger Converter from input content.

```
POST https://connect.mindcloud.co/v1/universal/swaggerConverter/latest/actions/convert-definition-by-content
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Swagger Converter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/swaggerConverter/latest/actions/convert-definition-by-content" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "specification": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/swaggerConverter/latest/actions/convert-definition-by-content', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "specification": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `specification` | object | yes | The Swagger/OpenAPI 1.x or 2.x specification object to convert. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Swagger Converter API returns.

## Native endpoint

Through the native Swagger Converter API, this operation is `POST convert` (base URL `https://converter.swagger.io/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/convert-definition-by-content.md) for the provider-specific parameters and requirements.

