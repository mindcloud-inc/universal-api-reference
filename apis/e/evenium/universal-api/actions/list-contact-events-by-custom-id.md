# Evenium: List Contact Events by Custom ID

Retrieves a contact's events from Evenium by custom ID.

```
GET https://connect.mindcloud.co/v1/universal/evenium/latest/actions/list-contact-events-by-custom-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Evenium `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/evenium/latest/actions/list-contact-events-by-custom-id?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/evenium/latest/actions/list-contact-events-by-custom-id?${params}`, {
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
| `customId` | string | no | The Evenium Custom ID. |

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
      "registration": {},
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
| `registration` | object | Registration summary for the contact on the event. |
| `startDate` | date | Event start timestamp. |
| `status` | string | Evenium event status. |
| `title` | string | Event title. |
| `type` | string | Evenium event type. |
| `webSite` | string | Event website URL. |

## Native endpoint

Through the native Evenium API, this operation is `GET /contacts/customId/:customId/events` (base URL `https://evenium.com/api/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contact-events-by-custom-id.md) for the provider-specific parameters and requirements.

