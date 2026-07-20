# DialMyCalls: List Contacts in Group

Retrieves contacts from a specific DialMyCalls group.

```
GET https://connect.mindcloud.co/v1/universal/dialMyCalls/latest/actions/list-contacts-in-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DialMyCalls `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dialMyCalls/latest/actions/list-contacts-in-group?connectionId=$CONNECTION_ID&limit=25&offset=0&groupId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "groupId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dialMyCalls/latest/actions/list-contacts-in-group?${params}`, {
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
| `groupId` | string | yes | The DialMyCalls group ID whose contacts should be listed. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "extra1": "string",
      "firstname": "Ava",
      "groups": [
        {}
      ],
      "id": "string",
      "lastname": "Chen",
      "phone": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `email` | string |  |
| `extra1` | string |  |
| `firstname` | string |  |
| `groups` | array<object> |  |
| `id` | string |  |
| `lastname` | string |  |
| `phone` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native DialMyCalls API, this operation is `GET /contacts/:GroupId` (base URL `https://{{credentials.apiKey}}@api.dialmycalls.com/2.0`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-contacts-in-group.md) for the provider-specific parameters and requirements.

