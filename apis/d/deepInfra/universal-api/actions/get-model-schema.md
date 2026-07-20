# Deep Infra: Get Model Schema



```
GET https://connect.mindcloud.co/v1/universal/deepInfra/latest/actions/get-model-schema
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Deep Infra `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deepInfra/latest/actions/get-model-schema?connectionId=$CONNECTION_ID&modelName=Ava%20Chen&variantKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "modelName": "Ava Chen",
  "variantKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deepInfra/latest/actions/get-model-schema?${params}`, {
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
| `modelName` | string | yes | DeepInfra model identifier from the model URL path. |
| `variantKey` | string | yes | Schema variant key from the model schema URL path. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "fields_in": {
        "description": "string",
        "ftype": "string",
        "name": "Ava Chen"
      },
      "schema_in": {},
      "schema_out": {},
      "schema_stream": {},
      "variant": {
        "key": "string",
        "url": "https://example.com"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fields_in` | array<object> | Input field definitions. |
| `fields_in.description` | string | Input field description. |
| `fields_in.ftype` | string | Input field type. |
| `fields_in.name` | string | Input field name. |
| `schema_in` | object | Input JSON schema. |
| `schema_out` | object | Output JSON schema. |
| `schema_stream` | object | Streaming output JSON schema. |
| `variant` | object | Schema variant metadata. |
| `variant.key` | string | Schema variant key. |
| `variant.url` | string | Variant documentation or resource URL. |

## Native endpoint

Through the native Deep Infra API, this operation is `GET /models/:model_name/schema/:variantKey` (base URL `https://api.deepinfra.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-model-schema.md) for the provider-specific parameters and requirements.

