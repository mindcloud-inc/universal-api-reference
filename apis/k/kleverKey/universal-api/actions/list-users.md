# KleverKey: List Users



```
GET https://connect.mindcloud.co/v1/universal/kleverKey/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KleverKey `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kleverKey/latest/actions/list-users?connectionId=$CONNECTION_ID&limit=25&offset=0&organizationId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "organizationId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kleverKey/latest/actions/list-users?${params}`, {
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
| `organizationId` | number | yes | Organization ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accessGroups": [
        {}
      ],
      "cultureCode": "string",
      "displayName": "Ava Chen",
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": 1,
      "lastName": "Chen",
      "organizationIds": [
        1
      ],
      "roles": [
        {}
      ],
      "type": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accessGroups` | array<object> |  |
| `cultureCode` | string |  |
| `displayName` | string |  |
| `email` | string |  |
| `firstName` | string |  |
| `id` | number |  |
| `lastName` | string |  |
| `organizationIds` | array<number> |  |
| `roles` | array<object> |  |
| `type` | number |  |

## Native endpoint

Through the native KleverKey API, this operation is `GET /api/v1/organizations/:organizationId/users` (base URL `https://api.kleverkey.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

