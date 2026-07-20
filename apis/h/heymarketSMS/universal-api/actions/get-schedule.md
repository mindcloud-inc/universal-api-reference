# Heymarket SMS: Get Schedule



```
GET https://connect.mindcloud.co/v1/universal/heymarketSMS/latest/actions/get-schedule
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Heymarket SMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/heymarketSMS/latest/actions/get-schedule?connectionId=$CONNECTION_ID&scheduleId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "scheduleId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/heymarketSMS/latest/actions/get-schedule?${params}`, {
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
| `scheduleId` | number | yes | Unique identifier of the schedule. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "2026-05-07T12:00:00.000Z",
      "execute": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "inbox_id": 1,
      "local_id": "string",
      "meta": {},
      "op": "string",
      "team_id": 1,
      "updated": "2026-05-07T12:00:00.000Z",
      "user_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | date |  |
| `execute` | date |  |
| `id` | number |  |
| `inbox_id` | number |  |
| `local_id` | string |  |
| `meta` | object |  |
| `op` | string |  |
| `team_id` | number |  |
| `updated` | date |  |
| `user_id` | number |  |

## Native endpoint

Through the native Heymarket SMS API, this operation is `GET /v1/schedule/:id` (base URL `https://api.heymarket.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-schedule.md) for the provider-specific parameters and requirements.

