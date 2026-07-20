# Evenium: List Event Part Registrations

Retrieves event part registrations from Evenium.

```
GET https://connect.mindcloud.co/v1/universal/evenium/latest/actions/list-event-part-registrations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Evenium `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/evenium/latest/actions/list-event-part-registrations?connectionId=$CONNECTION_ID&limit=25&offset=0&eventId=1&eventPartId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "eventId": "1",
  "eventPartId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/evenium/latest/actions/list-event-part-registrations?${params}`, {
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
| `eventId` | number | yes | The Evenium eventId. |
| `eventPartId` | number | yes | The Evenium eventPartId. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "category": {},
      "contactId": 1,
      "creationDate": "2026-05-07T12:00:00.000Z",
      "eventPartId": 1,
      "lastUpdate": "2026-05-07T12:00:00.000Z",
      "personId": 1,
      "postStatus": "string",
      "seatCount": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `category` | object | Evenium category object. |
| `contactId` | number | Contact ID. |
| `creationDate` | date | Registration creation timestamp. |
| `eventPartId` | number | Event part ID. |
| `lastUpdate` | date | Last modification timestamp. |
| `personId` | number | Underlying person ID. |
| `postStatus` | string | Post-event attendance status. |
| `seatCount` | number | Reserved seat count. |
| `status` | string | Guest registration status. |

## Native endpoint

Through the native Evenium API, this operation is `GET /events/:eventId/eventParts/:eventPartId/registrations` (base URL `https://evenium.com/api/1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-event-part-registrations.md) for the provider-specific parameters and requirements.

