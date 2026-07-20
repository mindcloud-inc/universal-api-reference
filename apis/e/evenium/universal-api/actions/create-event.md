# Evenium: Create Event

Creates a new event in Evenium.

```
POST https://connect.mindcloud.co/v1/universal/evenium/latest/actions/create-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Evenium `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/evenium/latest/actions/create-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/evenium/latest/actions/create-event', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "creationDate": "2026-05-07T12:00:00.000Z",
      "displayTitle": "string",
      "endDate": "2026-05-07T12:00:00.000Z",
      "facets": [
        "string"
      ],
      "fields": [
        {}
      ],
      "id": 1,
      "locales": [
        "string"
      ],
      "location": {},
      "startDate": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "title": "string",
      "type": "string",
      "webSite": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string | Evenium event code. |
| `creationDate` | date | Event creation timestamp. |
| `displayTitle` | string | Display title. |
| `endDate` | date | Event end timestamp. |
| `facets` | array<string> | Enabled event facets. |
| `fields` | array<object> | Additional Evenium event fields. |
| `id` | number | Evenium event ID. |
| `locales` | array<string> | Configured event locales. |
| `location` | object | Event location object. |
| `startDate` | date | Event start timestamp. |
| `status` | string | Evenium event status. |
| `title` | string | Event title. |
| `type` | string | Evenium event type. |
| `webSite` | string | Event website URL. |

## Native endpoint

Through the native Evenium API, this operation is `POST https://evenium.com/api/2/member/events` (base URL `https://evenium.com/api/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-event.md) for the provider-specific parameters and requirements.

