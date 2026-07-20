# Booqable: List Customers

Retrieves customer records from Booqable.

```
GET https://connect.mindcloud.co/v1/universal/booqable/latest/actions/list-customers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Booqable `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/booqable/latest/actions/list-customers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/booqable/latest/actions/list-customers?${params}`, {
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
| `fields.customers` | string | no | Comma-separated customer fields to include instead of the default field set. |
| `filter` | object | no | Field-qualified customer filters using Booqable filter syntax. |
| `include` | string | no | Comma-separated relationships to sideload. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "archived": true,
        "createdAt": "2026-05-07T12:00:00.000Z",
        "depositType": "string",
        "depositValue": 1,
        "discountPercentage": 1,
        "email": "ava@example.com",
        "legalType": "string",
        "name": "Ava Chen",
        "number": 1,
        "orderCount": 1,
        "properties": {},
        "tagList": [
          "string"
        ],
        "updatedAt": "2026-05-07T12:00:00.000Z"
      },
      "id": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.archived` | boolean | Whether the customer is archived. |
| `attributes.createdAt` | date | When the customer was created. |
| `attributes.depositType` | string | Default deposit type. |
| `attributes.depositValue` | number | Default deposit value. |
| `attributes.discountPercentage` | number | Default discount percentage. |
| `attributes.email` | string | Customer email address. |
| `attributes.legalType` | string | Customer legal type. |
| `attributes.name` | string | Customer name. |
| `attributes.number` | number | Customer number. |
| `attributes.orderCount` | number | Number of orders. |
| `attributes.properties` | object | Custom properties. |
| `attributes.tagList` | array<string> | Customer tags. |
| `attributes.updatedAt` | date | When the customer was last updated. |
| `id` | string | Customer ID. |
| `type` | string | Resource type. |

## Native endpoint

Through the native Booqable API, this operation is `GET /customers` (base URL `https://mindcloud.booqable.com/api/4`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-customers.md) for the provider-specific parameters and requirements.

