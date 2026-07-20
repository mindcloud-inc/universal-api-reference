# Apideck: List custom mappings

Retrieves custom mappings from Apideck Vault.

```
GET https://connect.mindcloud.co/v1/universal/apideck/latest/actions/custommappingsall
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Apideck `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/apideck/latest/actions/custommappingsall?connectionId=$CONNECTION_ID&unified_api=string&service_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "unified_api": "string",
  "service_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/apideck/latest/actions/custommappingsall?${params}`, {
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
| `unified_api` | string | yes |  |
| `service_id` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "consumer_id": "string",
      "custom_field": true,
      "description": "string",
      "example": "string",
      "id": "string",
      "key": "string",
      "label": "string",
      "required": true,
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `consumer_id` | string |  |
| `custom_field` | boolean |  |
| `description` | string |  |
| `example` | string |  |
| `id` | string |  |
| `key` | string |  |
| `label` | string |  |
| `required` | boolean |  |
| `value` | string |  |

## Native endpoint

Through the native Apideck API, this operation is `GET /vault/custom-mappings/:unified_api/:service_id` (base URL `https://unify.apideck.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/custommappingsall.md) for the provider-specific parameters and requirements.

