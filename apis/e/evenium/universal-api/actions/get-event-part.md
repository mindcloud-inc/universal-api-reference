# Evenium: Get Event Part

Retrieves an event part from Evenium.

```
GET https://connect.mindcloud.co/v1/universal/evenium/latest/actions/get-event-part
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Evenium `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/evenium/latest/actions/get-event-part?connectionId=$CONNECTION_ID&eventId=1&eventPartId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "eventId": "1",
  "eventPartId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/evenium/latest/actions/get-event-part?${params}`, {
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
      "code": "string",
      "displayInProgram": true,
      "displayTitle": "string",
      "endDate": "2026-05-07T12:00:00.000Z",
      "eventId": 1,
      "fields": [
        {}
      ],
      "id": 1,
      "lastUpdate": "2026-05-07T12:00:00.000Z",
      "location": {},
      "nature": "string",
      "startDate": "2026-05-07T12:00:00.000Z",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string | Event part code. |
| `displayInProgram` | boolean | Whether the event part is visible in the program. |
| `displayTitle` | string | Event part display title. |
| `endDate` | date | Event part end timestamp. |
| `eventId` | number | Parent event ID. |
| `fields` | array<object> | Additional event part fields. |
| `id` | number | Event part ID. |
| `lastUpdate` | date | Last modification timestamp. |
| `location` | object | Event part location object. |
| `nature` | string | Event part nature. |
| `startDate` | date | Event part start timestamp. |
| `title` | string | Event part title. |

## Native endpoint

Through the native Evenium API, this operation is `GET /events/:eventId/eventParts/:eventPartId` (base URL `https://evenium.com/api/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-event-part.md) for the provider-specific parameters and requirements.

