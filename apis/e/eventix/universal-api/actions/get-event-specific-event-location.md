# Eventix: Get Location of Event

Retrieves the location of an Eventix event.

```
GET https://connect.mindcloud.co/v1/universal/eventix/latest/actions/get-event-specific-event-location
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Eventix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eventix/latest/actions/get-event-specific-event-location?connectionId=$CONNECTION_ID&guid=event-guid" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "guid": "event-guid"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eventix/latest/actions/get-event-specific-event-location?${params}`, {
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
      "address": "string",
      "capacity": 1,
      "company_id": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "deleted_at": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "guid": "string",
      "latitude": 1,
      "longitude": 1,
      "name": "Ava Chen",
      "parent_guid": "string",
      "public": true,
      "seated": true,
      "seats_chart_key": "string",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string |  |
| `capacity` | number |  |
| `company_id` | string |  |
| `created_at` | date |  |
| `deleted_at` | date |  |
| `description` | string |  |
| `guid` | string |  |
| `latitude` | number |  |
| `longitude` | number |  |
| `name` | string |  |
| `parent_guid` | string |  |
| `public` | boolean |  |
| `seated` | boolean |  |
| `seats_chart_key` | string |  |
| `updated_at` | date |  |

## Native endpoint

Through the native Eventix API, this operation is `GET /3.0.0/event/:guid/location` (base URL `https://api.weeztix.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-event-specific-event-location.md) for the provider-specific parameters and requirements.

