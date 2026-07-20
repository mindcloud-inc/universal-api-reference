# ProdPad: List Feedback

Retrieves feedback from ProdPad.

```
GET https://connect.mindcloud.co/v1/universal/prodPad/latest/actions/list-feedback
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProdPad `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/prodPad/latest/actions/list-feedback?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/prodPad/latest/actions/list-feedback?${params}`, {
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
| `groupBy` | string | no |  |
| `state` | string | no |  |
| `company` | string | no |  |
| `customer` | string | no |  |
| `product` | string | no |  |
| `persona` | string | no |  |
| `jobRole` | string | no |  |
| `tags` | string | no | Accepts multiple values in one string, delimited by `,`. |
| `hasIdeas` | boolean | no |  |
| `externalId` | string | no |  |
| `externalUrl` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "added_by": {
        "display_name": "Ava Chen",
        "id": 1,
        "username": "Ava Chen"
      },
      "created_at": "2026-05-07T12:00:00.000Z",
      "customer": {
        "about": "string",
        "created_at": "2026-05-07T12:00:00.000Z",
        "email": "ava@example.com",
        "id": 1,
        "name": "Ava Chen",
        "updated_at": "2026-05-07T12:00:00.000Z"
      },
      "feedback": "string",
      "id": 1,
      "source": "string",
      "state": "string",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `added_by.display_name` | string |  |
| `added_by.id` | number |  |
| `added_by.username` | string |  |
| `created_at` | date |  |
| `customer.about` | string |  |
| `customer.created_at` | date |  |
| `customer.email` | string |  |
| `customer.id` | number |  |
| `customer.name` | string |  |
| `customer.updated_at` | date |  |
| `feedback` | string |  |
| `id` | number |  |
| `source` | string |  |
| `state` | string |  |
| `updated_at` | date |  |
| `uuid` | string |  |

## Native endpoint

Through the native ProdPad API, this operation is `GET /feedbacks` (base URL `https://api.prodpad.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-feedback.md) for the provider-specific parameters and requirements.

