# Castor EDC: Replace Study User Roles

Updates study user roles in Castor EDC.

```
PUT https://connect.mindcloud.co/v1/universal/castorEDC/latest/actions/replace-study-user-roles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Castor EDC `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/castorEDC/latest/actions/replace-study-user-roles" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "studyId": "string",
  "userId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/castorEDC/latest/actions/replace-study-user-roles', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "studyId": "string",
    "userId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `studyId` | string | yes | The Castor study UUID. |
| `userId` | string | yes | The study user UUID. |
| `managePermissions` | object | no | Management permission flags as an object. |
| `roleAssignments[]` | array<object> | no | Array of role assignment objects with site_id and role_name. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `defaultRoleAssignment` | number | no | Default site role identifier. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Castor EDC API returns.

## Native endpoint

Through the native Castor EDC API, this operation is `PUT /study/:study_id/user/:user_id` (base URL `https://us.castoredc.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/replace-study-user-roles.md) for the provider-specific parameters and requirements.

