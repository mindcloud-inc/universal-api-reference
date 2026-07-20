# Grand Avenue Software: List Users

Retrieves users from Grand Avenue Software.

```
GET https://connect.mindcloud.co/v1/universal/grandAvenueSoftware/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Grand Avenue Software `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/grandAvenueSoftware/latest/actions/list-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/grandAvenueSoftware/latest/actions/list-users?${params}`, {
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
| `filter` | string | no | e.g. `UpdatedTimestamp > 2025-12-18T00:00:00.000Z` |
| `Select` | list<string> | no | Accepts multiple values as an array. |
| `expand` | list<string> | no | Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountType": "string",
      "active": "string",
      "apiVersion": 1,
      "createdDate": "string",
      "departmentDisplay": "string",
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": 1,
      "lastName": "Chen",
      "updatedTimestamp": "2026-05-07T12:00:00.000Z",
      "userID": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountType` | string |  |
| `active` | string |  |
| `apiVersion` | number |  |
| `createdDate` | string |  |
| `departmentDisplay` | string |  |
| `email` | string |  |
| `firstName` | string |  |
| `id` | number |  |
| `lastName` | string |  |
| `updatedTimestamp` | date |  |
| `userID` | string |  |

## Native endpoint

Through the native Grand Avenue Software API, this operation is `GET /Users` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

