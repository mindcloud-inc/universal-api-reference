# MoreApp: List Group Users

Retrieves users in a MoreApp group.

```
GET https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/list-group-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MoreApp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/list-group-users?connectionId=$CONNECTION_ID&customerId=1&groupId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerId": "1",
  "groupId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/list-group-users?${params}`, {
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
| `customerId` | number | yes |  |
| `groupId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "disabled": true,
      "externallyManaged": true,
      "firstName": "Ava",
      "id": "string",
      "lastName": "Chen",
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `disabled` | boolean |  |
| `externallyManaged` | boolean |  |
| `firstName` | string |  |
| `id` | string |  |
| `lastName` | string |  |
| `username` | string |  |

## Native endpoint

Through the native MoreApp API, this operation is `GET /api/v2/customers/{{customerId}}/groups/{{groupId}}/users` (base URL `https://api.moreapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-group-users.md) for the provider-specific parameters and requirements.

