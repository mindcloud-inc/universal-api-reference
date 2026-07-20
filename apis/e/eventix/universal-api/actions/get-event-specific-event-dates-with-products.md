# Eventix: Get EventDates for Event with Products

Retrieves event dates with products for an Eventix event.

```
GET https://connect.mindcloud.co/v1/universal/eventix/latest/actions/get-event-specific-event-dates-with-products
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Eventix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eventix/latest/actions/get-event-specific-event-dates-with-products?connectionId=$CONNECTION_ID&guid=event-guid" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "guid": "event-guid"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eventix/latest/actions/get-event-specific-event-dates-with-products?${params}`, {
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
| `guid` | string | yes | The guid of the Event. Example: `event-guid`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "capacity": 1,
      "end": "2026-05-07T12:00:00.000Z",
      "event_id": "string",
      "facebook_event_id": "string",
      "guid": "string",
      "products": [
        {}
      ],
      "seated": true,
      "seats_event_key": "string",
      "start": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `capacity` | number |  |
| `end` | date |  |
| `event_id` | string |  |
| `facebook_event_id` | string |  |
| `guid` | string |  |
| `products` | array<object> |  |
| `seated` | boolean |  |
| `seats_event_key` | string |  |
| `start` | date |  |

## Native endpoint

Through the native Eventix API, this operation is `GET /3.0.0/event/:guid/dates/products` (base URL `https://api.weeztix.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-event-specific-event-dates-with-products.md) for the provider-specific parameters and requirements.

