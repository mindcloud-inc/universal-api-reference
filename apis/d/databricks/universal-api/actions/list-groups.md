# Databricks: List Groups

Retrieves groups from the Databricks account.

```
GET https://connect.mindcloud.co/v1/universal/databricks/latest/actions/list-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Databricks `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/databricks/latest/actions/list-groups?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/databricks/latest/actions/list-groups?${params}`, {
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
| `filter` | string | no | Query by which the results have to be filtered. Supported operators are equals(`eq`), contains(`co`), starts with(`sw`) and not equals(`ne`). Additionally, simple expressions can be formed using logical operators - `and` and `or`. The [SCIM RFC](https://tools.ietf.org/html/rfc7644#section-3.4.2.2) has more details but we currently only support simple expressions. |
| `attributes` | string | no | Comma-separated list of attributes to return in response. |
| `excludedattributes` | string | no | Comma-separated list of attributes to exclude in response. |
| `startindex` | number | no | Specifies the index of the first result. First item is number 1. |
| `count` | number | no | Desired number of results per page. Default is 10000. |
| `sortby` | string | no | Attribute to sort the results. |
| `sortorder` | string | no | The order to sort the results. |

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

Through the native Databricks API, this operation is `GET /api/2.0/accounts/{{credentials.accountId}}/scim/v2/Groups` (base URL `https://accounts.cloud.databricks.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-groups.md) for the provider-specific parameters and requirements.

