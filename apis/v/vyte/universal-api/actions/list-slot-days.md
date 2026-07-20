# Vyte: List Slot Days

Retrieves slot days from Vyte.

```
GET https://connect.mindcloud.co/v1/universal/vyte/latest/actions/list-slot-days
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vyte `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vyte/latest/actions/list-slot-days?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vyte/latest/actions/list-slot-days?${params}`, {
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
| `emails` | string | no | Comma-separated email list to evaluate daily availability for. Default: `apps@mindcloud.co`. |
| `from` | string | no | Start date or datetime for the search window. Default: `2026-04-01`. |
| `to` | string | no | End date or datetime for the search window. Default: `2026-04-02`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "days": {},
      "from": "string",
      "to": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `days` | object |  |
| `from` | string |  |
| `to` | string |  |

## Native endpoint

Through the native Vyte API, this operation is `GET v2/slots/days` (base URL `https://api.vyte.in`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-slot-days.md) for the provider-specific parameters and requirements.

