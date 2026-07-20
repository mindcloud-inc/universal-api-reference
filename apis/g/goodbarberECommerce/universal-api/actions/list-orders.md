# Goodbarber eCommerce: List Orders



```
GET https://connect.mindcloud.co/v1/universal/goodbarberECommerce/latest/actions/list-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Goodbarber eCommerce `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goodbarberECommerce/latest/actions/list-orders?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goodbarberECommerce/latest/actions/list-orders?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `creationDateFrom` | string | no | Restricts the list of returned orders to the ones created after (or on) the provided datetime. This parameter should use the following format yyyy-mm-ddThh:MM (year, month, day, 24-hour and minute) and be expressed in UTC time. |
| `creationDateTo` | string | no | Restricts the list of returned orders to the ones created before (or on) the provided datetime. This parameter should use the following format yyyy-mm-ddThh:MM (year, month, day, 24-hour and minute) and be expressed in UTC time. |
| `deliveryDateFrom` | string | no | Restricts the list of returned orders to the ones whose selected delivery slot lands after (or on) the provided datetime. This parameter should use the following format yyyy-mm-ddThh:MM (year, month, day, 24-hour and minute) and be expressed in UTC time. When this filter is applied, orders that do not have a selected delivery slot (shipped by transporter, for instance) will not be returned. Also, note that a delivery slot is said to land after a given datetime if its slot_start value is later than that datetime. |
| `deliveryDateTo` | string | no | Restricts the list of returned orders to the ones whose selected delivery slot lands before (or on) the provided datetime. This parameter should use the following format yyyy-mm-ddThh:MM (year, month, day, 24-hour and minute) and be expressed in UTC time. When this filter is applied, orders that do not have a selected delivery slot (shipped by transporter, for instance) will not be returned. Also, note that a delivery slot is said to land before a given datetime if its slot_end value comes before that datetime. |
| `status` | string | no | Restricts the list of returned orders to a certain status. To filter several statuses use the following syntax: ?status={STATUS1}&status={STATUS2} |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "next": "string",
      "orders": [
        {}
      ],
      "previous": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number | <div class="field_description">Number of orders returned by the API.</div> |
| `next` | string | <div class="field_description">URL to access the next page of the orders list.</div> |
| `orders` | array<object> | <div class="field_description">List of orders.</div> |
| `previous` | string | <div class="field_description">URL to access the previous page of the orders list.</div> |

## Native endpoint

Through the native Goodbarber eCommerce API, this operation is `GET /publicapi/v2/general/orders/:webzine_id/` (base URL `https://commerce.goodbarber.dev`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-orders.md) for the provider-specific parameters and requirements.

