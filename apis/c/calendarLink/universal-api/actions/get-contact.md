# CalendarLink: Get Contact

Retrieves a contact from a CalendarLink organization.

```
GET https://connect.mindcloud.co/v1/universal/calendarLink/latest/actions/get-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CalendarLink `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/calendarLink/latest/actions/get-contact?connectionId=$CONNECTION_ID&contact=string&organization=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contact": "string",
  "organization": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/calendarLink/latest/actions/get-contact?${params}`, {
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
| `contact` | string | yes | CalendarLink contact ID. |
| `organization` | string | yes | CalendarLink organization ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "activitiesCount": "string",
      "country": "string",
      "email": "ava@example.com",
      "eventsCount": "string",
      "id": "string",
      "name": "Ava Chen",
      "notes": "string",
      "phone": "string",
      "registrationsCount": "string",
      "subscriptionsCount": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activitiesCount` | string |  |
| `country` | string |  |
| `email` | string |  |
| `eventsCount` | string |  |
| `id` | string |  |
| `name` | string |  |
| `notes` | string |  |
| `phone` | string |  |
| `registrationsCount` | string |  |
| `subscriptionsCount` | string |  |

## Native endpoint

Through the native CalendarLink API, this operation is `GET /:organisation/contact/:contact` (base URL `https://my.calendarlink.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact.md) for the provider-specific parameters and requirements.

