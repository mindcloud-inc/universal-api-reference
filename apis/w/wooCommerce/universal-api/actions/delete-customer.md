# WooCommerce: Delete Customer

Deletes an existing customer from WooCommerce.

```
DELETE https://connect.mindcloud.co/v1/universal/wooCommerce/latest/actions/delete-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WooCommerce `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/wooCommerce/latest/actions/delete-customer?connectionId=$CONNECTION_ID&force=true&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "force": "true",
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wooCommerce/latest/actions/delete-customer?${params}`, {
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
| `force` | boolean | yes | Required to be true because customer deletion does not support trashing. |
| `id` | list<number> | yes | Unique numeric ID of the customer to delete. |
| `reassign` | number | no | User ID to reassign posts to when deleting a customer. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "avatarUrl": "https://example.com",
      "billing": {},
      "dateCreated": "2026-05-07T12:00:00.000Z",
      "dateCreatedGmt": "2026-05-07T12:00:00.000Z",
      "dateModified": "2026-05-07T12:00:00.000Z",
      "dateModifiedGmt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": 1,
      "isPayingCustomer": true,
      "lastName": "Chen",
      "metaData": [
        {}
      ],
      "role": "string",
      "shipping": {},
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avatarUrl` | string |  |
| `billing` | object |  |
| `dateCreated` | date |  |
| `dateCreatedGmt` | date |  |
| `dateModified` | date |  |
| `dateModifiedGmt` | date |  |
| `email` | string |  |
| `firstName` | string |  |
| `id` | number |  |
| `isPayingCustomer` | boolean |  |
| `lastName` | string |  |
| `metaData` | array<object> |  |
| `role` | string |  |
| `shipping` | object |  |
| `username` | string |  |

## Native endpoint

Through the native WooCommerce API, this operation is `DELETE /customers/:id` (base URL `{{credentials.siteUrl}}/wp-json/wc/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-customer.md) for the provider-specific parameters and requirements.

