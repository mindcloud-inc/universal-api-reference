# ActivityInfo: List Database Users

Retrieves users for a specific ActivityInfo database.

```
GET https://connect.mindcloud.co/v1/universal/activityInfo/latest/actions/list-database-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ActivityInfo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/activityInfo/latest/actions/list-database-users?connectionId=$CONNECTION_ID&databaseId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "databaseId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/activityInfo/latest/actions/list-database-users?${params}`, {
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
| `databaseId` | string | yes | ActivityInfo database ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "activationStatus": "string",
      "databaseId": "string",
      "email": "ava@example.com",
      "name": "Ava Chen",
      "role": {},
      "userId": "string",
      "userLicenseType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activationStatus` | string | Account activation status. |
| `databaseId` | string | Database ID. |
| `email` | string | User email. |
| `name` | string | User name. |
| `role` | object | Assigned role. |
| `userId` | string | User ID. |
| `userLicenseType` | string | Required license type. |

## Native endpoint

Through the native ActivityInfo API, this operation is `GET /resources/databases/:databaseId/users` (base URL `https://www.activityinfo.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-database-users.md) for the provider-specific parameters and requirements.

