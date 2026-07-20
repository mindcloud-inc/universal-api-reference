# Knack: Update User Roles On Account



```
PUT https://connect.mindcloud.co/v1/universal/knack/latest/actions/update-user-roles-on-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Knack `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/knack/latest/actions/update-user-roles-on-account" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "objectKey": "string",
  "recordId": "string",
  "userRolesFieldKey": "field_5",
  "userRoleProfileKeys[]": "profile_4"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/knack/latest/actions/update-user-roles-on-account', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "objectKey": "string",
    "recordId": "string",
    "userRolesFieldKey": "field_5",
    "userRoleProfileKeys[]": "profile_4"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `objectKey` | string | yes | User object key, such as object_1. |
| `recordId` | string | yes | User account record ID to update. |
| `userRolesFieldKey` | string | yes | Target Knack user roles field key, such as field_5. Example: `field_5`. |
| `userRoleProfileKeys[]` | array<string> | yes | One or more Knack profile IDs to assign, such as profile_4. Example: `profile_4`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Knack API returns.

## Native endpoint

Through the native Knack API, this operation is `PUT /objects/:object_key/records/:record_id` (base URL `https://api.knack.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-user-roles-on-account.md) for the provider-specific parameters and requirements.

