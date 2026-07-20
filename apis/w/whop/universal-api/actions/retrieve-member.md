# Whop: Retrieve Member

Retrieves member details from the Whop platform.

```
GET https://connect.mindcloud.co/v1/universal/whop/latest/actions/retrieve-member
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Whop `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/whop/latest/actions/retrieve-member?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/whop/latest/actions/retrieve-member?${params}`, {
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
| `id` | string | yes | The unique identifier of the member. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accessLevel": "string",
      "company": {
        "id": "string",
        "route": "string",
        "title": "string"
      },
      "companyTokenBalance": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "joinedAt": "2026-05-07T12:00:00.000Z",
      "mostRecentAction": "string",
      "mostRecentActionAt": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "usdTotalSpent": 1,
      "user": {
        "email": "ava@example.com",
        "id": "string",
        "name": "Ava Chen",
        "username": "Ava Chen"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accessLevel` | string |  |
| `company` | object |  |
| `company.id` | string |  |
| `company.route` | string |  |
| `company.title` | string |  |
| `companyTokenBalance` | number |  |
| `createdAt` | date |  |
| `id` | string |  |
| `joinedAt` | date |  |
| `mostRecentAction` | string |  |
| `mostRecentActionAt` | date |  |
| `status` | string |  |
| `updatedAt` | date |  |
| `usdTotalSpent` | number |  |
| `user` | object |  |
| `user.email` | string |  |
| `user.id` | string |  |
| `user.name` | string |  |
| `user.username` | string |  |

## Native endpoint

Through the native Whop API, this operation is `GET /api/v1/members/:id` (base URL `https://api.whop.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-member.md) for the provider-specific parameters and requirements.

