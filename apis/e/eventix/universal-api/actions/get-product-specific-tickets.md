# Eventix: Get Ticket Types of Product Type

Retrieves ticket types for an Eventix product type.

```
GET https://connect.mindcloud.co/v1/universal/eventix/latest/actions/get-product-specific-tickets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Eventix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eventix/latest/actions/get-product-specific-tickets?connectionId=$CONNECTION_ID&guid=product-guid" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "guid": "product-guid"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eventix/latest/actions/get-product-specific-tickets?${params}`, {
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
| `guid` | string | yes | The guid of the Product Type. Example: `product-guid`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "available_from": "2026-05-07T12:00:00.000Z",
      "available_until": "2026-05-07T12:00:00.000Z",
      "class": "string",
      "combines_products": true,
      "company_id": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "event_id": "string",
      "guid": "string",
      "hide_without_coupon": true,
      "increment": 1,
      "late_personalization": true,
      "min_price": 1,
      "name": "Ava Chen",
      "seated": true,
      "status": "string",
      "status_overrule": "string",
      "swappable": true,
      "updated_at": "2026-05-07T12:00:00.000Z",
      "vat_percentage": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `available_from` | date |  |
| `available_until` | date |  |
| `class` | string |  |
| `combines_products` | boolean |  |
| `company_id` | string |  |
| `created_at` | date |  |
| `description` | string |  |
| `event_id` | string |  |
| `guid` | string |  |
| `hide_without_coupon` | boolean |  |
| `increment` | number |  |
| `late_personalization` | boolean |  |
| `min_price` | number |  |
| `name` | string |  |
| `seated` | boolean |  |
| `status` | string |  |
| `status_overrule` | string |  |
| `swappable` | boolean |  |
| `updated_at` | date |  |
| `vat_percentage` | number |  |

## Native endpoint

Through the native Eventix API, this operation is `GET /3.0.0/product/:guid/tickets` (base URL `https://api.weeztix.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-product-specific-tickets.md) for the provider-specific parameters and requirements.

