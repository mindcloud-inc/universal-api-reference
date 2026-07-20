# Apideck: Get consent records

Retrieves consent records from Apideck Vault.

```
GET https://connect.mindcloud.co/v1/universal/apideck/latest/actions/connectionconsentsall
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Apideck `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/apideck/latest/actions/connectionconsentsall?connectionId=$CONNECTION_ID&service_id=string&unified_api=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "service_id": "string",
  "unified_api": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/apideck/latest/actions/connectionconsentsall?${params}`, {
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
| `service_id` | string | yes |  |
| `unified_api` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "string",
      "granted": true,
      "id": "string",
      "resources": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | string |  |
| `granted` | boolean |  |
| `id` | string |  |
| `resources` | object |  |

## Native endpoint

Through the native Apideck API, this operation is `GET /vault/connections/:unified_api/:service_id/consent` (base URL `https://unify.apideck.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/connectionconsentsall.md) for the provider-specific parameters and requirements.

