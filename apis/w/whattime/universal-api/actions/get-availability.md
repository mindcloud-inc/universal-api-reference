# Whattime: Get Availability



```
GET https://connect.mindcloud.co/v1/universal/whattime/latest/actions/get-availability
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Whattime `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/whattime/latest/actions/get-availability?connectionId=$CONNECTION_ID&code=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "code": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/whattime/latest/actions/get-availability?${params}`, {
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
| `code` | string | yes | Resource Code |

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

Through the native Whattime API, this operation is `GET /availabilities/:code` (base URL `https://api.whattime.co.kr/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-availability.md) for the provider-specific parameters and requirements.

