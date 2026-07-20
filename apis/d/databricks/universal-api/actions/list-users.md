# Databricks: List Users

Retrieves users from the Databricks account.

```
GET https://connect.mindcloud.co/v1/universal/databricks/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Databricks `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/databricks/latest/actions/list-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/databricks/latest/actions/list-users?${params}`, {
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
| `attributes` | string | no | Comma-separated list of attributes to return in response. |
| `count` | number | no | Desired number of results per page. Default is 10000. |
| `excludedattributes` | string | no | Comma-separated list of attributes to exclude in response. |
| `filter` | string | no | Query by which the results have to be filtered. Supported operators are equals(`eq`), contains(`co`), starts with(`sw`) and not equals(`ne`). Additionally, simple expressions can be formed using logical operators - `and` and `or`. The [SCIM RFC](https://tools.ietf.org/html/rfc7644#section-3.4.2.2) has more details but we currently only support simple expressions. |
| `sortby` | string | no | Attribute to sort the results. Multi-part paths are supported. For example, `userName`, `name.givenName`, and `emails`. |
| `sortorder` | string | no | The order to sort the results. |
| `startindex` | number | no | Specifies the index of the first result. First item is number 1. |

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

Through the native Databricks API, this operation is `GET /api/2.0/accounts/{{credentials.accountId}}/scim/v2/Users` (base URL `https://accounts.cloud.databricks.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

