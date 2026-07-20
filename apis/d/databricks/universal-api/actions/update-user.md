# Databricks: Update User

Updates an existing user in the Databricks account.

```
PUT https://connect.mindcloud.co/v1/universal/databricks/latest/actions/update-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Databricks `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/databricks/latest/actions/update-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "userId": "string",
  "operations": "string",
  "schemas": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/databricks/latest/actions/update-user', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "userId": "string",
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
| `userId` | string | yes | Unique ID in the Databricks workspace. |
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
      "id": "string",
      "userName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean | Whether the user is active. |
| `id` | string | Databricks user ID. |
| `userName` | string | Email address of the Databricks user. |

## Native endpoint

Through the native Databricks API, this operation is `PATCH /api/2.0/accounts/{{credentials.accountId}}/scim/v2/Users/:userId` (base URL `https://accounts.cloud.databricks.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-user.md) for the provider-specific parameters and requirements.

