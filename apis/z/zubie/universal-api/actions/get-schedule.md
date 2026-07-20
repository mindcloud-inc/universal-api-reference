# Zubie: Get Schedule

Retrieves a schedule from Zubie.

```
GET https://connect.mindcloud.co/v1/universal/zubie/latest/actions/get-schedule
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zubie `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zubie/latest/actions/get-schedule?connectionId=$CONNECTION_ID&schedule_key=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "schedule_key": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zubie/latest/actions/get-schedule?${params}`, {
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
| `schedule_key` | string | yes | Unique schedule key. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "category": "string",
      "key": "string",
      "name": "Ava Chen",
      "periods": [
        {}
      ],
      "updated": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `category` | string |  |
| `key` | string |  |
| `name` | string |  |
| `periods` | array<object> |  |
| `updated` | string |  |

## Native endpoint

Through the native Zubie API, this operation is `GET /schedule/{schedule_key}` (base URL `https://api.zubiecar.com/api/v2/zinc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-schedule.md) for the provider-specific parameters and requirements.

