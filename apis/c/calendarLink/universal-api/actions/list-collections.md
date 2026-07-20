# CalendarLink: List Collections

Retrieves collections from a CalendarLink organization.

```
GET https://connect.mindcloud.co/v1/universal/calendarLink/latest/actions/list-collections
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CalendarLink `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/calendarLink/latest/actions/list-collections?connectionId=$CONNECTION_ID&organization=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organization": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/calendarLink/latest/actions/list-collections?${params}`, {
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
| `organization` | string | yes | CalendarLink organization ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "activeSubscribersCount": 1,
      "description": "string",
      "eventsCount": 1,
      "id": "string",
      "name": "Ava Chen",
      "publicUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activeSubscribersCount` | number |  |
| `description` | string |  |
| `eventsCount` | number |  |
| `id` | string |  |
| `name` | string |  |
| `publicUrl` | string |  |

## Native endpoint

Through the native CalendarLink API, this operation is `GET /:organisation/collection` (base URL `https://my.calendarlink.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-collections.md) for the provider-specific parameters and requirements.

