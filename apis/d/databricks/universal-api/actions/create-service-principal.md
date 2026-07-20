# Databricks: Create Service Principal

Creates a new service principal in the Databricks account.

```
POST https://connect.mindcloud.co/v1/universal/databricks/latest/actions/create-service-principal
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Databricks `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/databricks/latest/actions/create-service-principal" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "roles": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/databricks/latest/actions/create-service-principal', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "roles": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `active` | boolean | no | If this user is active |
| `applicationid` | string | no | UUID relating to the service principal |
| `displayname` | string | no | String that represents a concatenation of given and family names. |
| `externalid` | string | no |  |
| `id` | string | no | Databricks service principal ID. |
| `roles` | list<string> | yes | Indicates if the group has the admin role. |
| `roles[].ref` | string | no |  |
| `roles[].display` | string | no |  |
| `roles[].primary` | boolean | no |  |
| `roles[].type` | string | no |  |
| `roles[].value` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "$ref": "string",
      "display": "string",
      "primary": true,
      "type": "string",
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `$ref` | string |  |
| `display` | string |  |
| `primary` | boolean |  |
| `type` | string |  |
| `value` | string |  |

## Native endpoint

Through the native Databricks API, this operation is `POST /api/2.0/accounts/{{credentials.accountId}}/scim/v2/ServicePrincipals` (base URL `https://accounts.cloud.databricks.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-service-principal.md) for the provider-specific parameters and requirements.

