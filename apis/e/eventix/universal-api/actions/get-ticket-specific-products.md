# Eventix: Retrieve all Product Types attached to this Ticket Type

Retrieves product types for an Eventix ticket type.

```
GET https://connect.mindcloud.co/v1/universal/eventix/latest/actions/get-ticket-specific-products
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Eventix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eventix/latest/actions/get-ticket-specific-products?connectionId=$CONNECTION_ID&guid=ticket-guid" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "guid": "ticket-guid"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eventix/latest/actions/get-ticket-specific-products?${params}`, {
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
| `guid` | string | yes | The guid of the Ticket Type. Example: `ticket-guid`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "class": "string",
      "description": "string",
      "event_id": "string",
      "guid": "string",
      "name": "Ava Chen",
      "origin_type": "string",
      "price": 1,
      "pricing_method": "string",
      "skip_late_personalization": true,
      "status": "string",
      "vat_percentage": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `class` | string |  |
| `description` | string |  |
| `event_id` | string |  |
| `guid` | string |  |
| `name` | string |  |
| `origin_type` | string |  |
| `price` | number |  |
| `pricing_method` | string |  |
| `skip_late_personalization` | boolean |  |
| `status` | string |  |
| `vat_percentage` | number |  |

## Native endpoint

Through the native Eventix API, this operation is `GET /3.0.0/ticket/:guid/products` (base URL `https://api.weeztix.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-ticket-specific-products.md) for the provider-specific parameters and requirements.

