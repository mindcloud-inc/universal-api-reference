# Frontegg: List Tenants

Finds accounts in your Frontegg environment.

```
GET https://connect.mindcloud.co/v1/universal/frontegg/latest/actions/list-tenants
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Frontegg `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/frontegg/latest/actions/list-tenants?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/frontegg/latest/actions/list-tenants?${params}`, {
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
| `limit` | number | no | Maximum number of tenants to return (default 50, maximum 200). |
| `offset` | number | no | Page number to retrieve, starting at 0. |
| `filter` | string | no | Filter tenants by name or tenant ID. |
| `sortBy` | string | no | Sort by createdAt, name, or tenantId. |
| `order` | string | no | Sort order: ASC or DESC. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tenantIds` | string | no | Specific tenant IDs to retrieve. |

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

Through the native Frontegg API, this operation is `GET /tenants/resources/tenants/v2` (base URL `https://api.frontegg.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-tenants.md) for the provider-specific parameters and requirements.

