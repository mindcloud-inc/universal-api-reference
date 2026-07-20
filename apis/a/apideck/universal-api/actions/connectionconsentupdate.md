# Apideck: Update consent state

Updates a connection consent state in Apideck Vault.

```
PUT https://connect.mindcloud.co/v1/universal/apideck/latest/actions/connectionconsentupdate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Apideck `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/apideck/latest/actions/connectionconsentupdate" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "service_id": "string",
  "unified_api": "string",
  "resources": {},
  "granted": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/apideck/latest/actions/connectionconsentupdate', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "service_id": "string",
    "unified_api": "string",
    "resources": {},
    "granted": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `service_id` | string | yes |  |
| `unified_api` | string | yes |  |
| `resources` | object | yes |  |
| `granted` | boolean | yes |  |

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

Through the native Apideck API, this operation is `PATCH /vault/connections/:unified_api/:service_id/consent` (base URL `https://unify.apideck.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/connectionconsentupdate.md) for the provider-specific parameters and requirements.

