# Databricks: Update Service Principal

Updates an existing service principal in the Databricks account.

```
PUT https://connect.mindcloud.co/v1/universal/databricks/latest/actions/update-service-principal
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Databricks `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/databricks/latest/actions/update-service-principal" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "servicePrincipalId": "string",
  "operations": "string",
  "schemas": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/databricks/latest/actions/update-service-principal', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "servicePrincipalId": "string",
    "operations": "string",
    "schemas": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `servicePrincipalId` | string | yes | Unique ID in the Databricks workspace. |
| `operations` | list<string> | yes |  |
| `operations[].op` | string | no | Type of patch operation. |
| `operations[].path` | string | no | Selection of patch operation |
| `operations[].value` | string | no | Value to modify |
| `schemas` | list<string> | yes | The schema of the patch request. Must be ["urn:ietf:params:scim:api:messages:2.0:PatchOp"]. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "applicationId": "string",
      "displayName": "Ava Chen",
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean | Whether the service principal is active. |
| `applicationId` | string | Application ID for the service principal. |
| `displayName` | string | Service principal display name. |
| `id` | string | Databricks service principal ID. |

## Native endpoint

Through the native Databricks API, this operation is `PATCH /api/2.0/accounts/{{credentials.accountId}}/scim/v2/ServicePrincipals/:servicePrincipalId` (base URL `https://accounts.cloud.databricks.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-service-principal.md) for the provider-specific parameters and requirements.

