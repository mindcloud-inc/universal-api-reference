# Fivetran: List Group Users

Retrieves users for a group in Fivetran.

```
GET https://connect.mindcloud.co/v1/universal/fivetran/latest/actions/list-group-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fivetran `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fivetran/latest/actions/list-group-users?connectionId=$CONNECTION_ID&limit=25&offset=0&groupId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "groupId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fivetran/latest/actions/list-group-users?${params}`, {
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
| `active` | boolean | no | Return only enabled users when true. |
| `groupId` | string | yes | The unique identifier for the group within Fivetran. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com",
      "familyName": "Ava Chen",
      "givenName": "Ava Chen",
      "id": "string",
      "role": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string |  |
| `familyName` | string |  |
| `givenName` | string |  |
| `id` | string |  |
| `role` | string |  |

## Native endpoint

Through the native Fivetran API, this operation is `GET /groups/[:groupId]/users` (base URL `https://api.fivetran.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-group-users.md) for the provider-specific parameters and requirements.

