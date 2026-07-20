# Databricks: Create Group

Creates a new group in the Databricks account.

```
POST https://connect.mindcloud.co/v1/universal/databricks/latest/actions/create-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Databricks `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/databricks/latest/actions/create-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "members": "string",
  "roles": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/databricks/latest/actions/create-group', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "members": "string",
    "roles": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `displayname` | string | no | String that represents a human-readable group name |
| `externalid` | string | no |  |
| `id` | string | no | Databricks group ID |
| `members` | list<string> | yes |  |
| `members[].ref` | string | no |  |
| `members[].display` | string | no |  |
| `members[].primary` | boolean | no |  |
| `members[].type` | string | no |  |
| `members[].value` | string | no |  |
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
      "account_id": "string",
      "displayName": "Ava Chen",
      "externalId": "string",
      "id": "string",
      "members": [
        {
          "$ref": "string",
          "display": "string",
          "primary": true,
          "type": "string",
          "value": "string"
        }
      ],
      "roles": [
        {
          "$ref": "string",
          "display": "string",
          "primary": true,
          "type": "string",
          "value": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account_id` | string | Databricks account ID |
| `displayName` | string | String that represents a human-readable group name |
| `externalId` | string | external_id should be unique for identifying groups |
| `id` | string | Databricks group ID |
| `members` | array<string> |  |
| `members[].$ref` | string |  |
| `members[].display` | string |  |
| `members[].primary` | boolean |  |
| `members[].type` | string |  |
| `members[].value` | string |  |
| `roles` | array<string> | Indicates if the group has the admin role. |
| `roles[].$ref` | string |  |
| `roles[].display` | string |  |
| `roles[].primary` | boolean |  |
| `roles[].type` | string |  |
| `roles[].value` | string |  |

## Native endpoint

Through the native Databricks API, this operation is `POST /api/2.0/accounts/{{credentials.accountId}}/scim/v2/Groups` (base URL `https://accounts.cloud.databricks.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-group.md) for the provider-specific parameters and requirements.

