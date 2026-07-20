# WaiverForever: Get Template Prefill Schema

Retrieves a template prefill schema from WaiverForever.

```
GET https://connect.mindcloud.co/v1/universal/waiverForever/latest/actions/get-template-prefill-schema
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WaiverForever `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/waiverForever/latest/actions/get-template-prefill-schema?connectionId=$CONNECTION_ID&templateId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "templateId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/waiverForever/latest/actions/get-template-prefill-schema?${params}`, {
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
| `templateId` | string | yes | WaiverForever template identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "$id": "string",
      "$schema": "string",
      "additionalProperties": true,
      "properties": {},
      "title": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `$id` | string | Schema identifier URL. |
| `$schema` | string | JSON Schema spec URL. |
| `additionalProperties` | boolean | Whether extra properties are allowed. |
| `properties` | object | Prefillable properties. |
| `title` | string | Schema title. |
| `type` | string | Top-level schema type. |

## Native endpoint

Through the native WaiverForever API, this operation is `GET /openapi/v2/template/:template_id/prefill/schema` (base URL `https://api.waiverforever.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-template-prefill-schema.md) for the provider-specific parameters and requirements.

