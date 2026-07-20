# Seven Time: List Customers

Retrieves customers from a Seven Time workspace.

```
GET https://connect.mindcloud.co/v1/universal/sevenTime/latest/actions/list-customers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Seven Time `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sevenTime/latest/actions/list-customers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sevenTime/latest/actions/list-customers?${params}`, {
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
| `name` | string | no |  |
| `customerNumber` | string | no |  |
| `organizationNumber` | string | no |  |
| `city` | string | no |  |
| `lastModified` | date | no | Return customers modified since the provided timestamp. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": "string",
      "billingSettings": {},
      "city": "string",
      "customerNumber": "string",
      "documents": [
        {}
      ],
      "email": "ava@example.com",
      "Id": "string",
      "name": "Ava Chen",
      "organizationNumber": "string",
      "phone": "string",
      "vatNumber": "string",
      "zipCode": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string |  |
| `billingSettings` | object |  |
| `city` | string |  |
| `customerNumber` | string |  |
| `documents` | array<object> |  |
| `email` | string |  |
| `Id` | string |  |
| `name` | string |  |
| `organizationNumber` | string |  |
| `phone` | string |  |
| `vatNumber` | string |  |
| `zipCode` | string |  |

## Native endpoint

Through the native Seven Time API, this operation is `GET /customers` (base URL `https://app.seventime.se/api/2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-customers.md) for the provider-specific parameters and requirements.

