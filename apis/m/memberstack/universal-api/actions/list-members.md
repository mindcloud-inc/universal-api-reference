# Memberstack: List Members



```
GET https://connect.mindcloud.co/v1/universal/memberstack/latest/actions/list-members
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Memberstack `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/memberstack/latest/actions/list-members?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/memberstack/latest/actions/list-members?${params}`, {
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
      "auth": {},
      "createdAt": "2026-05-07T12:00:00.000Z",
      "customFields": {},
      "id": "string",
      "lastLogin": "2026-05-07T12:00:00.000Z",
      "loginRedirect": "string",
      "metaData": {},
      "permissions": [
        "string"
      ],
      "planConnections": [
        {}
      ],
      "profileImage": "string",
      "stripeCustomerId": "string",
      "verified": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `auth` | object |  |
| `createdAt` | date |  |
| `customFields` | object |  |
| `id` | string |  |
| `lastLogin` | date |  |
| `loginRedirect` | string |  |
| `metaData` | object |  |
| `permissions` | array<string> |  |
| `planConnections` | array<object> |  |
| `profileImage` | string |  |
| `stripeCustomerId` | string |  |
| `verified` | boolean |  |

## Native endpoint

Through the native Memberstack API, this operation is `GET /members` (base URL `https://admin.memberstack.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-members.md) for the provider-specific parameters and requirements.

