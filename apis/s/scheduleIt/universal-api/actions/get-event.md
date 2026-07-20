# Schedule It: Get Event

Retrieves event details from Schedule It.

```
GET https://connect.mindcloud.co/v1/universal/scheduleIt/latest/actions/get-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Schedule It `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scheduleIt/latest/actions/get-event?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scheduleIt/latest/actions/get-event?${params}`, {
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
| `id` | number | yes | The event ID. |
| `fields` | string | no | Comma-separated list of fields to return. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "date_start": "string",
      "date_start_timezone": "string",
      "date_start_utc": "string",
      "id": "string",
      "timezone": "string",
      "title": "string",
      "workspace": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `date_start` | string |  |
| `date_start_timezone` | string |  |
| `date_start_utc` | string |  |
| `id` | string |  |
| `timezone` | string |  |
| `title` | string |  |
| `workspace` | string |  |

## Native endpoint

Through the native Schedule It API, this operation is `GET /events/:id` (base URL `https://www.scheduleit.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-event.md) for the provider-specific parameters and requirements.

