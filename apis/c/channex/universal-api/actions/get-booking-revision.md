# Channex: Get Booking Revision

Retrieves a booking revision from Channex.

```
GET https://connect.mindcloud.co/v1/universal/channex/latest/actions/get-booking-revision
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Channex `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/channex/latest/actions/get-booking-revision?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/channex/latest/actions/get-booking-revision?${params}`, {
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
| `id` | string | yes | UUID of the booking revision to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "attributes": {
          "amount": "string",
          "arrival_date": "2026-05-07T12:00:00.000Z",
          "booking_id": "string",
          "currency": "string",
          "departure_date": "2026-05-07T12:00:00.000Z",
          "property_id": "string",
          "status": "string"
        },
        "id": "string",
        "type": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.attributes.amount` | string |  |
| `data.attributes.arrival_date` | date |  |
| `data.attributes.booking_id` | string |  |
| `data.attributes.currency` | string |  |
| `data.attributes.departure_date` | date |  |
| `data.attributes.property_id` | string |  |
| `data.attributes.status` | string |  |
| `data.id` | string |  |
| `data.type` | string |  |

## Native endpoint

Through the native Channex API, this operation is `GET /booking_revisions/:id` (base URL `https://staging.channex.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-booking-revision.md) for the provider-specific parameters and requirements.

