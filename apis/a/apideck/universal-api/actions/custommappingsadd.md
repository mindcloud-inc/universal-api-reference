# Apideck: Create custom mapping

Creates a new custom mapping in Apideck Vault.

```
POST https://connect.mindcloud.co/v1/universal/apideck/latest/actions/custommappingsadd
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Apideck `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/apideck/latest/actions/custommappingsadd" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "unified_api": "string",
  "service_id": "string",
  "target_field_id": "string",
  "value": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/apideck/latest/actions/custommappingsadd', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "unified_api": "string",
    "service_id": "string",
    "target_field_id": "string",
    "value": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `unified_api` | string | yes |  |
| `service_id` | string | yes |  |
| `target_field_id` | string | yes |  |
| `value` | string | yes |  |

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

Through the native Apideck API, this operation is `POST /vault/custom-mappings/:unified_api/:service_id/:target_field_id` (base URL `https://unify.apideck.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/custommappingsadd.md) for the provider-specific parameters and requirements.

