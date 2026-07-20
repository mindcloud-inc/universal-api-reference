# Frontegg: Move Users Between Tenants

Moves users between accounts in Frontegg.

```
PUT https://connect.mindcloud.co/v1/universal/frontegg/latest/actions/move-users-between-tenants
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Frontegg `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/frontegg/latest/actions/move-users-between-tenants" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "srcTenantId": "string",
  "targetTenantId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/frontegg/latest/actions/move-users-between-tenants', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "srcTenantId": "string",
    "targetTenantId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `srcTenantId` | string | yes | Source tenant ID. |
| `targetTenantId` | string | yes | Target tenant ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Frontegg API returns.

## Native endpoint

Through the native Frontegg API, this operation is `PUT /identity/resources/users/v1/tenants/migrate` (base URL `https://api.frontegg.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/move-users-between-tenants.md) for the provider-specific parameters and requirements.

