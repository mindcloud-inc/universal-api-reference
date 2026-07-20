# Acronis: Disable Service For Sub-Tenant

Disables a service for a sub-tenant in Acronis.

```
DELETE https://connect.mindcloud.co/v1/universal/acronis/latest/actions/disable-service-for-sub-tenant
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Acronis `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/acronis/latest/actions/disable-service-for-sub-tenant?connectionId=$CONNECTION_ID&applicationId=string&tenantId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "applicationId": "string",
  "tenantId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/acronis/latest/actions/disable-service-for-sub-tenant?${params}`, {
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
| `applicationId` | string | yes | Application Id path parameter. |
| `tenantId` | string | yes | Tenant Id path parameter. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Acronis API returns.

## Native endpoint

Through the native Acronis API, this operation is `DELETE /api/2/applications/{application_id}/bindings/tenants/{tenant_id}` (base URL `{{credentials.dataCenterUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/disable-service-for-sub-tenant.md) for the provider-specific parameters and requirements.

