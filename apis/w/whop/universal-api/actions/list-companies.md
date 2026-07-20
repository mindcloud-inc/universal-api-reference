# Whop: List Companies

Retrieves companies from the Whop platform.

```
GET https://connect.mindcloud.co/v1/universal/whop/latest/actions/list-companies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Whop `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/whop/latest/actions/list-companies?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/whop/latest/actions/list-companies?${params}`, {
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": "string",
      "memberCount": 1,
      "ownerUser": {
        "id": "string",
        "name": "Ava Chen",
        "username": "Ava Chen"
      },
      "publishedReviewsCount": 1,
      "route": "string",
      "sendCustomerEmails": true,
      "title": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "verified": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `description` | string |  |
| `id` | string |  |
| `memberCount` | number |  |
| `ownerUser` | object |  |
| `ownerUser.id` | string |  |
| `ownerUser.name` | string |  |
| `ownerUser.username` | string |  |
| `publishedReviewsCount` | number |  |
| `route` | string |  |
| `sendCustomerEmails` | boolean |  |
| `title` | string |  |
| `updatedAt` | date |  |
| `verified` | boolean |  |

## Native endpoint

Through the native Whop API, this operation is `GET /api/v1/companies` (base URL `https://api.whop.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-companies.md) for the provider-specific parameters and requirements.

