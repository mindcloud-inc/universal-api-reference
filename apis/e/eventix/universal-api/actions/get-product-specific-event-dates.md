# Eventix: Get attached EventDates of Product Type

Retrieves event dates for an Eventix product type.

```
GET https://connect.mindcloud.co/v1/universal/eventix/latest/actions/get-product-specific-event-dates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Eventix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eventix/latest/actions/get-product-specific-event-dates?connectionId=$CONNECTION_ID&guid=product-guid" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "guid": "product-guid"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eventix/latest/actions/get-product-specific-event-dates?${params}`, {
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
      "capacity": 1,
      "end": "2026-05-07T12:00:00.000Z",
      "event_id": "string",
      "facebook_event_id": "string",
      "guid": "string",
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
| `seated` | boolean |  |
| `seats_event_key` | string |  |
| `start` | date |  |

## Native endpoint

Through the native Eventix API, this operation is `GET /3.0.0/product/:guid/dates` (base URL `https://api.weeztix.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-product-specific-event-dates.md) for the provider-specific parameters and requirements.

