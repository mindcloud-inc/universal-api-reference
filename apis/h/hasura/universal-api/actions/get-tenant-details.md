# Hasura: Get Tenant Details

Retrieves tenant details from Hasura Cloud.

```
GET https://connect.mindcloud.co/v1/universal/hasura/latest/actions/get-tenant-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hasura `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hasura/latest/actions/get-tenant-details?connectionId=$CONNECTION_ID&tenantId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "tenantId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hasura/latest/actions/get-tenant-details?${params}`, {
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
| `tenantId` | string | yes | Hasura Cloud tenant ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "tenant_by_pk": {
          "active": true,
          "cloud": "string",
          "fqdn": "string",
          "id": "string",
          "project_id": "string",
          "project": {
            "endpoint": "string",
            "id": "string",
            "name": "Ava Chen"
          },
          "region": "string",
          "slug": "string"
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.tenant_by_pk.active` | boolean | Whether the tenant is active. |
| `data.tenant_by_pk.cloud` | string | Tenant cloud provider. |
| `data.tenant_by_pk.fqdn` | string | Tenant fully qualified domain name. |
| `data.tenant_by_pk.id` | string | Tenant ID. |
| `data.tenant_by_pk.project_id` | string | Associated project ID. |
| `data.tenant_by_pk.project.endpoint` | string | Project endpoint. |
| `data.tenant_by_pk.project.id` | string | Project ID. |
| `data.tenant_by_pk.project.name` | string | Project name. |
| `data.tenant_by_pk.region` | string | Tenant cloud region. |
| `data.tenant_by_pk.slug` | string | Tenant slug. |

## Native endpoint

Through the native Hasura API, this operation is `POST /v1/graphql` (base URL `https://data.pro.hasura.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-tenant-details.md) for the provider-specific parameters and requirements.

