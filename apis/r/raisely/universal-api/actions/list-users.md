# Raisely: List Users

Retrieves users from Raisely.

```
GET https://connect.mindcloud.co/v1/universal/raisely/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Raisely `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/raisely/latest/actions/list-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/raisely/latest/actions/list-users?${params}`, {
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
| `private` | boolean | no | Returns the full record when authenticated |
| `q` | string | no | Search query to find records matching |
| `postcode` | string | no | Filter User based on their postcode value |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `country` | string | no | Filter User based on their country value |
| `facebookId` | string | no | Filter User based on their facebookId value |
| `email` | string | no | Filter User based on their email value |
| `fullName` | string | no | Filter User based on their fullName value |
| `phoneNumber` | string | no | Filter User based on their phone_number value |
| `organisation` | string | no | Filter by organisation uuid |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "firstName": "Ava",
      "organisationUuid": "string",
      "permission": "string",
      "photoUrl": "https://example.com",
      "preferredName": "Ava Chen",
      "status": "string",
      "tags": [
        "string"
      ],
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `firstName` | string |  |
| `organisationUuid` | string |  |
| `permission` | string |  |
| `photoUrl` | string |  |
| `preferredName` | string |  |
| `status` | string |  |
| `tags` | array<string> |  |
| `updatedAt` | date |  |
| `uuid` | string |  |

## Native endpoint

Through the native Raisely API, this operation is `GET /users` (base URL `https://api.raisely.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

