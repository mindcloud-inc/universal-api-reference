# Aspire: List Users

Creates a new pay code in your Aspire account.

```
GET https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aspire `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-users?${params}`, {
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
| `expand` | string | no |  |
| `filter` | string | no |  |
| `orderBy` | string | no |  |
| `select` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allBranchAccess": true,
      "userID": 1,
      "externalContactReference": "string",
      "contactFirstName": "Ava",
      "contactLastName": "Chen",
      "active": true,
      "userRoles": [
        {
          "roleID": 1,
          "roleName": "Ava Chen"
        }
      ],
      "branchAccess": [
        [
          "string"
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allBranchAccess` | boolean |  |
| `userID` | number |  |
| `externalContactReference` | string |  |
| `contactFirstName` | string |  |
| `contactLastName` | string |  |
| `active` | boolean |  |
| `userRoles[].roleID` | number |  |
| `userRoles[].roleName` | string |  |
| `userRoles[]` | array | The roles assigned to this user in Aspire. |
| `branchAccess[]` | array | When allBranchAccess is 'false' a list of individual branch access is provided. |

## Native endpoint

Through the native Aspire API, this operation is `GET Users` (base URL `https://{{credentials.environment}}.youraspire.com/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

