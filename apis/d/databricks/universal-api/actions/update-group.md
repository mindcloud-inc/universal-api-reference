# Databricks: Update Group

Updates an existing group in the Databricks account.

```
PUT https://connect.mindcloud.co/v1/universal/databricks/latest/actions/update-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Databricks `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/databricks/latest/actions/update-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "groupId": "string",
  "operations": "string",
  "schemas": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/databricks/latest/actions/update-group', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "groupId": "string",
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
| `groupId` | string | yes | Unique ID in the Databricks workspace. |
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
      "displayName": "Ava Chen",
      "id": "string",
      "roles": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `displayName` | string | Human-readable group name. |
| `id` | string | Databricks group ID. |
| `roles` | array<string> | Group roles. |

## Native endpoint

Through the native Databricks API, this operation is `PATCH /api/2.0/accounts/{{credentials.accountId}}/scim/v2/Groups/:groupId` (base URL `https://accounts.cloud.databricks.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-group.md) for the provider-specific parameters and requirements.

