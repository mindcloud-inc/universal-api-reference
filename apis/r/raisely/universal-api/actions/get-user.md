# Raisely: Get User

Retrieves a user from Raisely.

```
GET https://connect.mindcloud.co/v1/universal/raisely/latest/actions/get-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Raisely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/raisely/latest/actions/get-user?connectionId=$CONNECTION_ID&uuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "uuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/raisely/latest/actions/get-user?${params}`, {
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
| `uuid` | string | yes | The `uuid` of the record |
| `private` | boolean | no | Returns the full record when authenticated |

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

Through the native Raisely API, this operation is `GET /users/:uuid` (base URL `https://api.raisely.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user.md) for the provider-specific parameters and requirements.

