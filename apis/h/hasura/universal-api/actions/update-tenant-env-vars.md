# Hasura: Update Tenant ENV Vars

Updates tenant environment variables in Hasura Cloud.

```
PUT https://connect.mindcloud.co/v1/universal/hasura/latest/actions/update-tenant-env-vars
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hasura `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/hasura/latest/actions/update-tenant-env-vars" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "tenantId": "string",
  "currentHash": "string",
  "envs[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hasura/latest/actions/update-tenant-env-vars', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "tenantId": "string",
    "currentHash": "string",
    "envs[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tenantId` | string | yes | Hasura Cloud tenant ID. |
| `currentHash` | string | yes | Current environment hash from Get Tenant ENV Vars. |
| `envs[]` | array<object> | yes | Replacement environment variables as objects with key and value fields. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "updateTenantEnv": {
          "envVars": [
            {}
          ],
          "hash": "string"
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
| `data.updateTenantEnv.envVars` | array<object> | Updated tenant environment variables. |
| `data.updateTenantEnv.hash` | string | Updated tenant environment variable hash. |

## Native endpoint

Through the native Hasura API, this operation is `POST /v1/graphql` (base URL `https://data.pro.hasura.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-tenant-env-vars.md) for the provider-specific parameters and requirements.

