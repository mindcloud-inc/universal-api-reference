# Whop: List Memberships

Retrieves memberships from Whop for a company.

```
GET https://connect.mindcloud.co/v1/universal/whop/latest/actions/list-memberships
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Whop `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/whop/latest/actions/list-memberships?connectionId=$CONNECTION_ID&companyId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "companyId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/whop/latest/actions/list-memberships?${params}`, {
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
| `companyId` | string | yes | The unique identifier of the company to list memberships for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cancelAtPeriodEnd": true,
      "company": {
        "id": "string",
        "title": "string"
      },
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "joinedAt": "2026-05-07T12:00:00.000Z",
      "licenseKey": "string",
      "manageUrl": "https://example.com",
      "paymentCollectionPaused": true,
      "product": {
        "id": "string",
        "title": "string"
      },
      "status": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "user": {
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
| `cancelAtPeriodEnd` | boolean |  |
| `company` | object |  |
| `company.id` | string |  |
| `company.title` | string |  |
| `createdAt` | date |  |
| `id` | string |  |
| `joinedAt` | date |  |
| `licenseKey` | string |  |
| `manageUrl` | string |  |
| `paymentCollectionPaused` | boolean |  |
| `product` | object |  |
| `product.id` | string |  |
| `product.title` | string |  |
| `status` | string |  |
| `updatedAt` | date |  |
| `user` | object |  |
| `user.id` | string |  |
| `user.name` | string |  |
| `user.username` | string |  |

## Native endpoint

Through the native Whop API, this operation is `GET /api/v1/memberships` (base URL `https://api.whop.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-memberships.md) for the provider-specific parameters and requirements.

