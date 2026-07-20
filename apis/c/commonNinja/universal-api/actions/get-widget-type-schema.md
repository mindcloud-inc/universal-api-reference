# Common Ninja: Get Widget Type Schema

Retrieves a widget type schema from Common Ninja.

```
GET https://connect.mindcloud.co/v1/universal/commonNinja/latest/actions/get-widget-type-schema
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Common Ninja `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/commonNinja/latest/actions/get-widget-type-schema?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/commonNinja/latest/actions/get-widget-type-schema?${params}`, {
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
| `id` | string | yes | The widget type ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "$id": "string",
      "$schema": "string",
      "allOf": [
        {}
      ],
      "definitions": {},
      "properties": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `$id` | string |  |
| `$schema` | string |  |
| `allOf` | array<object> |  |
| `definitions` | object |  |
| `properties` | object |  |

## Native endpoint

Through the native Common Ninja API, this operation is `GET /widget-types/:id/schema` (base URL `https://api.commoninja.com/platform/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-widget-type-schema.md) for the provider-specific parameters and requirements.

