# Erase.bg: Get Transformation Module

Retrieves a transformation module from Erase.bg.

```
GET https://connect.mindcloud.co/v1/universal/erasebg/latest/actions/get-transformation-module
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Erase.bg `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/erasebg/latest/actions/get-transformation-module?connectionId=$CONNECTION_ID&identifier=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "identifier": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/erasebg/latest/actions/get-transformation-module?${params}`, {
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
| `identifier` | string | yes | Transformation module identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "credentials": [
        {}
      ],
      "credits": 1,
      "description": "string",
      "enabled": true,
      "identifier": "string",
      "isBulkSupported": true,
      "name": "Ava Chen",
      "operations": [
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
| `credentials` | array<object> |  |
| `credits` | number |  |
| `description` | string |  |
| `enabled` | boolean |  |
| `identifier` | string |  |
| `isBulkSupported` | boolean |  |
| `name` | string |  |
| `operations` | array<object> |  |

## Native endpoint

Through the native Erase.bg API, this operation is `GET /service/platform/assets/v1.0/playground/plugins/:identifier` (base URL `https://api.pixelbin.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-transformation-module.md) for the provider-specific parameters and requirements.

