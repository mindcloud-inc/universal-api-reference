# Mailchimp: List Customers

Retrieves customers from a Mailchimp e-commerce store.

```
GET https://connect.mindcloud.co/v1/universal/mailChimp/latest/actions/list-customers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mailchimp `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailChimp/latest/actions/list-customers?connectionId=$CONNECTION_ID&limit=25&offset=0&store_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "store_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailChimp/latest/actions/list-customers?${params}`, {
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
| `email_address` | string | no |  |
| `exclude_fields` | string | no |  |
| `fields` | string | no |  |
| `store_id` | string | yes | The store id. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "customers": [
        [
          {}
        ]
      ],
      "links": {},
      "storeId": "string",
      "totalItems": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customers[]` | array<object> | Collection of customers. |
| `links` | object | Link relations. |
| `storeId` | string | The store id. |
| `totalItems` | number | Total number of customers. |

## Native endpoint

Through the native Mailchimp API, this operation is `GET ecommerce/stores/:store_id/customers` (base URL `https://{{credentials.serverPrefix}}.api.mailchimp.com/3.0/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-customers.md) for the provider-specific parameters and requirements.

