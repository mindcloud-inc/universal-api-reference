# Databricks: Create User

Creates a new user in the Databricks account.

```
POST https://connect.mindcloud.co/v1/universal/databricks/latest/actions/create-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Databricks `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/databricks/latest/actions/create-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "emails": "ava@example.com",
  "roles": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/databricks/latest/actions/create-user', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "emails": "ava@example.com",
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
| `displayname` | string | no | String that represents a concatenation of given and family names. For example `John Smith`. |
| `emails` | list<string> | yes | All the emails associated with the Databricks user. |
| `emails[].ref` | string | no |  |
| `emails[].display` | string | no |  |
| `emails[].primary` | boolean | no |  |
| `emails[].type` | string | no |  |
| `emails[].value` | string | no |  |
| `externalid` | string | no | External ID is not currently supported. It is reserved for future use. |
| `id` | string | no | Databricks user ID. |
| `name` | object | no |  |
| `name.familyname` | string | no | Family name of the Databricks user. |
| `name.givenname` | string | no | Given name of the Databricks user. |
| `roles` | list<string> | yes | Indicates if the group has the admin role. |
| `roles[].ref` | string | no |  |
| `roles[].display` | string | no |  |
| `roles[].primary` | boolean | no |  |
| `roles[].type` | string | no |  |
| `roles[].value` | string | no |  |
| `username` | string | no | Email address of the Databricks user. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "account_id": "string",
      "active": true,
      "displayName": "Ava Chen",
      "emails": [
        {
          "$ref": "ava@example.com",
          "display": "ava@example.com",
          "primary": true,
          "type": "ava@example.com",
          "value": "ava@example.com"
        }
      ],
      "externalId": "string",
      "id": "string",
      "name": {
        "familyName": "Ava Chen",
        "givenName": "Ava Chen"
      },
      "roles": [
        {
          "$ref": "string",
          "display": "string",
          "primary": true,
          "type": "string",
          "value": "string"
        }
      ],
      "userName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account_id` | string | Databricks account ID |
| `active` | boolean | If this user is active |
| `displayName` | string | String that represents a concatenation of given and family names. For example `John Smith`. |
| `emails` | array<string> | All the emails associated with the Databricks user. |
| `emails[].$ref` | string |  |
| `emails[].display` | string |  |
| `emails[].primary` | boolean |  |
| `emails[].type` | string |  |
| `emails[].value` | string |  |
| `externalId` | string | External ID is not currently supported. It is reserved for future use. |
| `id` | string | Databricks user ID. |
| `name` | object |  |
| `name.familyName` | string | Family name of the Databricks user. |
| `name.givenName` | string | Given name of the Databricks user. |
| `roles` | array<string> | Indicates if the group has the admin role. |
| `roles[].$ref` | string |  |
| `roles[].display` | string |  |
| `roles[].primary` | boolean |  |
| `roles[].type` | string |  |
| `roles[].value` | string |  |
| `userName` | string | Email address of the Databricks user. |

## Native endpoint

Through the native Databricks API, this operation is `POST /api/2.0/accounts/{{credentials.accountId}}/scim/v2/Users` (base URL `https://accounts.cloud.databricks.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-user.md) for the provider-specific parameters and requirements.

