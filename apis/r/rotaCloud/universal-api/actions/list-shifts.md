# RotaCloud: List Shifts

Lists shifts in RotaCloud.

```
GET https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/list-shifts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RotaCloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/list-shifts?connectionId=$CONNECTION_ID&start=1&end=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "start": "1",
  "end": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/list-shifts?${params}`, {
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
| `start` | number | yes | Unix timestamp for the start of the shift window. |
| `end` | number | yes | Unix timestamp for the end of the shift window. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "acknowledged": true,
      "claimed": true,
      "created_at": 1,
      "deleted": true,
      "end_time": 1,
      "id": 1,
      "location": 1,
      "minutes_break": 1,
      "notes": "string",
      "open": true,
      "published": true,
      "role": 1,
      "start_time": 1,
      "swap_requests": [
        1
      ],
      "unavailability_requests": [
        1
      ],
      "user": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `acknowledged` | boolean |  |
| `claimed` | boolean |  |
| `created_at` | number |  |
| `deleted` | boolean |  |
| `end_time` | number |  |
| `id` | number |  |
| `location` | number |  |
| `minutes_break` | number |  |
| `notes` | string |  |
| `open` | boolean |  |
| `published` | boolean |  |
| `role` | number |  |
| `start_time` | number |  |
| `swap_requests` | array<number> |  |
| `unavailability_requests` | array<number> |  |
| `user` | number |  |

## Native endpoint

Through the native RotaCloud API, this operation is `GET /v1/shifts` (base URL `https://api.rotacloud.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-shifts.md) for the provider-specific parameters and requirements.

