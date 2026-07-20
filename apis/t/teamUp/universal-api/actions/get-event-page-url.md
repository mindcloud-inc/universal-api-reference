# TeamUp: Get Event Page URL

Retrieves the page URL for a TeamUp event.

```
GET https://connect.mindcloud.co/v1/universal/teamUp/latest/actions/get-event-page-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TeamUp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/teamUp/latest/actions/get-event-page-url?connectionId=$CONNECTION_ID&eventId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "eventId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/teamUp/latest/actions/get-event-page-url?${params}`, {
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
| `eventId` | string | yes | The TeamUp event identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "pointer": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `pointer` | string |  |
| `url` | string |  |

## Native endpoint

Through the native TeamUp API, this operation is `POST /:calendarKey/events/:eventId/pointer` (base URL `https://api.teamup.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-event-page-url.md) for the provider-specific parameters and requirements.

