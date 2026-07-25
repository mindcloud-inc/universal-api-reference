# CompanyCam: List Groups



```
GET https://connect.mindcloud.co/v1/universal/companyCam/latest/actions/list-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CompanyCam `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/companyCam/latest/actions/list-groups?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/companyCam/latest/actions/list-groups?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "companyId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "groupUrl": "https://example.com",
      "id": "string",
      "name": "Ava Chen",
      "status": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "users": [
        {
          "companyId": "string",
          "createdAt": "2026-05-07T12:00:00.000Z",
          "emailAddress": "ava@example.com",
          "firstName": "Ava",
          "id": "string",
          "lastName": "Chen",
          "phoneNumber": "string",
          "status": "string",
          "updatedAt": "2026-05-07T12:00:00.000Z",
          "userRole": "string",
          "userUrl": "https://example.com"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `companyId` | string |  |
| `createdAt` | date |  |
| `groupUrl` | string |  |
| `id` | string |  |
| `name` | string |  |
| `status` | string |  |
| `updatedAt` | date |  |
| `users[].companyId` | string |  |
| `users[].createdAt` | date |  |
| `users[].emailAddress` | string |  |
| `users[].firstName` | string |  |
| `users[].id` | string |  |
| `users[].lastName` | string |  |
| `users[].phoneNumber` | string |  |
| `users[].status` | string |  |
| `users[].updatedAt` | date |  |
| `users[].userRole` | string |  |
| `users[].userUrl` | string |  |

## Native endpoint

Through the native CompanyCam API, this operation is `GET groups` (base URL `https://api.companycam.com/v2/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-groups.md) for the provider-specific parameters and requirements.

