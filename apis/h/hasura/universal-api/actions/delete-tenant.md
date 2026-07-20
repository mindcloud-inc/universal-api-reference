# Hasura: Delete Tenant

Deletes a tenant from Hasura Cloud.

```
DELETE https://connect.mindcloud.co/v1/universal/hasura/latest/actions/delete-tenant
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hasura `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/hasura/latest/actions/delete-tenant?connectionId=$CONNECTION_ID&tenantId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "tenantId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hasura/latest/actions/delete-tenant?${params}`, {
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
| `tenantId` | string | yes | Hasura Cloud tenant ID to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "deleteTenant": {
          "status": "string"
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
| `data.deleteTenant.status` | string | Deletion status returned by Hasura Cloud. |

## Native endpoint

Through the native Hasura API, this operation is `POST /v1/graphql` (base URL `https://data.pro.hasura.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-tenant.md) for the provider-specific parameters and requirements.

