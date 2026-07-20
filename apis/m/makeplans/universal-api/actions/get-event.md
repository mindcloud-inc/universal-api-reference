# Makeplans: Get Event

Retrieves an event from Makeplans.

```
GET https://connect.mindcloud.co/v1/universal/makeplans/latest/actions/get-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Makeplans `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/makeplans/latest/actions/get-event?connectionId=$CONNECTION_ID&eventId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "eventId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/makeplans/latest/actions/get-event?${params}`, {
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
| `eventId` | number | yes | The Makeplans event ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "availability": 1,
      "capacity": 1,
      "description": "string",
      "ends_at": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "nr_of_attendances": 1,
      "published": true,
      "resource_id": 1,
      "service_id": 1,
      "starts_at": "2026-05-07T12:00:00.000Z",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `availability` | number |  |
| `capacity` | number |  |
| `description` | string |  |
| `ends_at` | date |  |
| `id` | number |  |
| `nr_of_attendances` | number |  |
| `published` | boolean |  |
| `resource_id` | number |  |
| `service_id` | number |  |
| `starts_at` | date |  |
| `title` | string |  |

## Native endpoint

Through the native Makeplans API, this operation is `GET /events/:eventId` (base URL `https://{{credentials.accountDomain}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-event.md) for the provider-specific parameters and requirements.

