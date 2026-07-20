# Databricks: Get Group

Retrieves a group from the Databricks account.

```
GET https://connect.mindcloud.co/v1/universal/databricks/latest/actions/get-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Databricks `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/databricks/latest/actions/get-group?connectionId=$CONNECTION_ID&groupId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "groupId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/databricks/latest/actions/get-group?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `groupId` | string | yes | Unique ID for a group in the Databricks account. |

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

Through the native Databricks API, this operation is `GET /api/2.0/accounts/{{credentials.accountId}}/scim/v2/Groups/:groupId` (base URL `https://accounts.cloud.databricks.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-group.md) for the provider-specific parameters and requirements.

