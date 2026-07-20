# 123FormBuild: Create Subuser

Creates a new subuser in 123FormBuilder.

```
POST https://connect.mindcloud.co/v1/universal/formBuild/latest/actions/create-subuser
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 123FormBuild `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/formBuild/latest/actions/create-subuser" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/formBuild/latest/actions/create-subuser', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | no | Email for the new subuser |
| `name` | string | no | Name of the new subuser |
| `password` | string | no | Password for the new subuser |
| `passhash` | string | no | Hashed password for the new subuser |
| `admin` | number | no | Admin flag for the subuser |
| `companyName` | string | no | Company name for the subuser |
| `allowCreateForm` | number | no | Permission to create forms |
| `allowDuplicateForm` | number | no | Permission to duplicate forms |
| `allowDeleteForm` | number | no | Permission to delete forms |
| `canManageGroups` | number | no | Permission to manage groups |
| `canManageUsers` | number | no | Permission to manage users |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native 123FormBuild API returns.

## Native endpoint

Through the native 123FormBuild API, this operation is `POST /users` (base URL `https://api.123formbuilder.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-subuser.md) for the provider-specific parameters and requirements.

