# Apideck: Get resource custom fields

Retrieves resource custom fields from Apideck Vault.

```
GET https://connect.mindcloud.co/v1/universal/apideck/latest/actions/customfieldsall
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Apideck `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/apideck/latest/actions/customfieldsall?connectionId=$CONNECTION_ID&unified_api=string&service_id=string&resource=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "unified_api": "string",
  "service_id": "string",
  "resource": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/apideck/latest/actions/customfieldsall?${params}`, {
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
| `resource` | string | yes |  |
| `resource_id` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "finder": "string",
      "id": "string",
      "name": "Ava Chen",
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `finder` | string |  |
| `id` | string |  |
| `name` | string |  |
| `value` | string |  |

## Native endpoint

Through the native Apideck API, this operation is `GET /vault/connections/:unified_api/:service_id/:resource/custom-fields` (base URL `https://unify.apideck.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/customfieldsall.md) for the provider-specific parameters and requirements.

