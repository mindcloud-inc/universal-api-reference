# Frontegg: Create Tenant

Creates a new account in Frontegg.

```
POST https://connect.mindcloud.co/v1/universal/frontegg/latest/actions/create-tenant
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Frontegg `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/frontegg/latest/actions/create-tenant" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/frontegg/latest/actions/create-tenant', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Account (tenant) name. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tenantId` | string | no | Optional unique tenant ID; Frontegg auto-generates one when omitted. |
| `creatorName` | string | no | Optional creator name for the tenant. |
| `creatorEmail` | string | no | Optional creator email for the tenant. |

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
| `createdAt` | date | Creation timestamp. |
| `deletedAt` | date | Deletion timestamp when present. |
| `id` | string | Internal record ID. |
| `name` | string | Tenant name. |
| `tenantId` | string | Tenant ID in Frontegg. |
| `updatedAt` | date | Last update timestamp. |
| `vendorId` | string | Vendor ID that owns the tenant. |

## Native endpoint

Through the native Frontegg API, this operation is `POST /tenants/resources/tenants/v1` (base URL `https://api.frontegg.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-tenant.md) for the provider-specific parameters and requirements.

