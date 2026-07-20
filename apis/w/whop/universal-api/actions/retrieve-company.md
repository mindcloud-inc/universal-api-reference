# Whop: Retrieve Company

Retrieves company details from the Whop platform.

```
GET https://connect.mindcloud.co/v1/universal/whop/latest/actions/retrieve-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Whop `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/whop/latest/actions/retrieve-company?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/whop/latest/actions/retrieve-company?${params}`, {
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
| `id` | string | yes | The unique identifier of the company. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
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
      "socialLinks": [
        "https://example.com"
      ],
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
| `id` | string |  |
| `memberCount` | number |  |
| `ownerUser` | object |  |
| `ownerUser.id` | string |  |
| `ownerUser.name` | string |  |
| `ownerUser.username` | string |  |
| `publishedReviewsCount` | number |  |
| `route` | string |  |
| `sendCustomerEmails` | boolean |  |
| `socialLinks` | array |  |
| `title` | string |  |
| `updatedAt` | date |  |
| `verified` | boolean |  |

## Native endpoint

Through the native Whop API, this operation is `GET /api/v1/companies/:id` (base URL `https://api.whop.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-company.md) for the provider-specific parameters and requirements.

