# Whattime: Create Availability



```
POST https://connect.mindcloud.co/v1/universal/whattime/latest/actions/create-availability
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Whattime `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/whattime/latest/actions/create-availability" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/whattime/latest/actions/create-availability', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `user` | string | no | User uri |
| `name` | string | yes | 이름 |
| `timeZone` | string | no | 타임존 |
| `default` | boolean | no | 기본 여부 |
| `rules[]` | array<object> | no | 요일별 가능한 시간 |
| `overrides[]` | array<object> | no | 가능한 시간 예외 날짜 |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "default": true,
      "name": "Ava Chen",
      "overrides": {
        "_destroy": true,
        "date": "2026-05-07T12:00:00.000Z",
        "intervals": {
          "end": "string",
          "start": "string"
        },
        "name": "Ava Chen"
      },
      "rules": {
        "end": "string",
        "start": "string",
        "wday": 1
      },
      "time_zone": "string",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "uri": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string |  |
| `created_at` | date |  |
| `default` | boolean |  |
| `name` | string |  |
| `overrides` | array<object> |  |
| `overrides._destroy` | boolean |  |
| `overrides.date` | date |  |
| `overrides.intervals` | array<object> |  |
| `overrides.intervals.end` | string |  |
| `overrides.intervals.start` | string |  |
| `overrides.name` | string |  |
| `rules` | array<object> |  |
| `rules.end` | string |  |
| `rules.start` | string |  |
| `rules.wday` | number |  |
| `time_zone` | string |  |
| `updated_at` | date |  |
| `uri` | string |  |

## Native endpoint

Through the native Whattime API, this operation is `POST /availabilities` (base URL `https://api.whattime.co.kr/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-availability.md) for the provider-specific parameters and requirements.

