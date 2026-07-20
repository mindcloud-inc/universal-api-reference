# Frontegg: Update Tenant

Updates an existing account in Frontegg.

```
PUT https://connect.mindcloud.co/v1/universal/frontegg/latest/actions/update-tenant
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Frontegg `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/frontegg/latest/actions/update-tenant" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "tenantId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/frontegg/latest/actions/update-tenant', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "tenantId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tenantId` | string | yes | The tenant ID to update. |
| `name` | string | no | Updated tenant name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "deletedAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "name": "Ava Chen",
      "tenantId": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "vendorId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `deletedAt` | date |  |
| `id` | string |  |
| `name` | string |  |
| `tenantId` | string |  |
| `updatedAt` | date |  |
| `vendorId` | string |  |

## Native endpoint

Through the native Frontegg API, this operation is `PUT /tenants/resources/tenants/v2/:tenantId` (base URL `https://api.frontegg.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-tenant.md) for the provider-specific parameters and requirements.

