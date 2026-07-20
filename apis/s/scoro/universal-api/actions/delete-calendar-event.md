# Scoro: Delete Calendar Event

Deletes an existing calendar event from Scoro.

```
DELETE https://connect.mindcloud.co/v1/universal/scoro/latest/actions/delete-calendar-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scoro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/scoro/latest/actions/delete-calendar-event?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scoro/latest/actions/delete-calendar-event?${params}`, {
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
| `id` | string | no | Scoro calendar event ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "messages": {},
      "status": "string",
      "statusCode": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `messages` | object | Scoro API messages payload. |
| `status` | string | Scoro API status. |
| `statusCode` | number | Scoro API status code. |

## Native endpoint

Through the native Scoro API, this operation is `POST calendar/delete/:id` (base URL `{{credentials.subdomain}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-calendar-event.md) for the provider-specific parameters and requirements.

