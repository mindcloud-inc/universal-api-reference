# GorillaDesk: List Customers

Retrieves customers from GorillaDesk.

```
GET https://connect.mindcloud.co/v1/universal/gorillaDesk/latest/actions/list-customers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GorillaDesk `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gorillaDesk/latest/actions/list-customers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gorillaDesk/latest/actions/list-customers?${params}`, {
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
| `accountNumber` | string | no | Return results where the account_number field is equal this value. |
| `created.gt` | date | no |  |
| `created.gte` | date | no |  |
| `created.lt` | date | no |  |
| `created.lte` | date | no |  |
| `include[]` | array<string> | no | Accepts multiple values in one string, delimited by `,`. |
| `state[]` | array<string> | no | Accepts multiple values in one string, delimited by `,`. |
| `status[]` | array<string> | no | Accepts multiple values in one string, delimited by `,`. |
| `updated.gt` | date | no |  |
| `updated.gte` | date | no |  |
| `updated.lt` | date | no |  |
| `updated.lte` | date | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountNumber": "string",
      "company": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": "string",
      "lastName": "Chen",
      "phones": [
        [
          {}
        ]
      ],
      "profileUrl": "https://example.com",
      "state": "string",
      "status": "string",
      "updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountNumber` | string |  |
| `company` | string |  |
| `created` | date |  |
| `email` | string |  |
| `firstName` | string |  |
| `id` | string |  |
| `lastName` | string |  |
| `phones[]` | array<object> |  |
| `phones[].id` | string |  |
| `phones[].phone` | string |  |
| `phones[].type` | string |  |
| `profileUrl` | string |  |
| `state` | string |  |
| `status` | string |  |
| `updated` | date |  |

## Native endpoint

Through the native GorillaDesk API, this operation is `GET /customers` (base URL `https://api.gorilladesk.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-customers.md) for the provider-specific parameters and requirements.

