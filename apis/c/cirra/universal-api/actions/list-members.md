# Cirra: List Members

Retrieves company member records from Cirra.

```
GET https://connect.mindcloud.co/v1/universal/cirra/latest/actions/list-members
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cirra `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cirra/latest/actions/list-members?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cirra/latest/actions/list-members?${params}`, {
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
      "isAdmin": true,
      "roleId": "string",
      "user": {
        "email": "ava@example.com",
        "isPending": true,
        "name": "Ava Chen"
      },
      "userId": "string",
      "workflowCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `companyId` | string |  |
| `isAdmin` | boolean |  |
| `roleId` | string |  |
| `user.email` | string |  |
| `user.isPending` | boolean |  |
| `user.name` | string |  |
| `userId` | string |  |
| `workflowCount` | number |  |

## Native endpoint

Through the native Cirra API, this operation is `GET /v1/members` (base URL `http://api-public:9801`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-members.md) for the provider-specific parameters and requirements.

