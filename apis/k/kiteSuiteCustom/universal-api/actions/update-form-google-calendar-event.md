# Kite Suite: Update Form Google Calendar Event



```
PUT https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/update-form-google-calendar-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kite Suite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/update-form-google-calendar-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "body": {},
  "id": "string",
  "title": "string",
  "startTime": "string",
  "endTime": "string",
  "location": "string",
  "description": "string",
  "createEventOnEdit": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/update-form-google-calendar-event', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "body": {},
    "id": "string",
    "title": "string",
    "startTime": "string",
    "endTime": "string",
    "location": "string",
    "description": "string",
    "createEventOnEdit": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `body` | object | yes | Request body |
| `id` | string | yes | ID of the Google Calendar event to update. |
| `title` | string | yes | Updated title of the Google Calendar event. |
| `startTime` | string | yes | Updated ID of the form element representing the start time. |
| `endTime` | string | yes | Updated ID of the form element representing the end time. |
| `location` | string | yes | Updated location of the Google Calendar event. |
| `description` | string | yes | Updated description of the Google Calendar event. |
| `createEventOnEdit` | boolean | yes | Updated flag to create event on form edit. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "value": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | object | Updated form integration object. |

## Native endpoint

Through the native Kite Suite API, this operation is `PATCH /api/v1/form/integration/google-calendar/events/:id` (base URL `https://api.kitesuite.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-form-google-calendar-event.md) for the provider-specific parameters and requirements.

