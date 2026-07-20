# Frontegg: Get Tenant

Retrieves an account in Frontegg by ID.

```
GET https://connect.mindcloud.co/v1/universal/frontegg/latest/actions/get-tenant
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Frontegg `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/frontegg/latest/actions/get-tenant?connectionId=$CONNECTION_ID&tenantId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "tenantId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/frontegg/latest/actions/get-tenant?${params}`, {
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
| `tenantId` | string | yes | The tenant ID to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "deletedAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "isReseller": true,
      "metadata": "string",
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
| `isReseller` | boolean |  |
| `metadata` | string |  |
| `name` | string |  |
| `tenantId` | string |  |
| `updatedAt` | date |  |
| `vendorId` | string |  |

## Native endpoint

Through the native Frontegg API, this operation is `GET /tenants/resources/tenants/v2/:tenantId` (base URL `https://api.frontegg.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-tenant.md) for the provider-specific parameters and requirements.

