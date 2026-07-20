# Vyte: List Available Slots

Retrieves available slots from Vyte.

```
GET https://connect.mindcloud.co/v1/universal/vyte/latest/actions/list-available-slots
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vyte `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vyte/latest/actions/list-available-slots?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vyte/latest/actions/list-available-slots?${params}`, {
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
| `duration` | string | no | Meeting duration in minutes. Default: `30`. |
| `emails` | string | no | Comma-separated email list to evaluate availability for. Default: `apps@mindcloud.co`. |
| `from` | string | no | Start date or datetime for the search window. Default: `2026-04-01`. |
| `to` | string | no | End date or datetime for the search window. Default: `2026-04-02`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "from": "string",
      "slots": [
        {}
      ],
      "timezone": "string",
      "to": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `from` | string |  |
| `slots` | array<object> |  |
| `timezone` | string |  |
| `to` | string |  |

## Native endpoint

Through the native Vyte API, this operation is `GET v2/slots` (base URL `https://api.vyte.in`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-available-slots.md) for the provider-specific parameters and requirements.

