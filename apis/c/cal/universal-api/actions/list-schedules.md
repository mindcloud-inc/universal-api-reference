# Cal.com: List Schedules

Retrieves schedules from Cal.com.

```
GET https://connect.mindcloud.co/v1/universal/cal/latest/actions/list-schedules
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cal.com `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cal/latest/actions/list-schedules?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cal/latest/actions/list-schedules?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "availability": [
        {}
      ],
      "id": 1,
      "isDefault": true,
      "name": "Ava Chen",
      "overrides": [
        {}
      ],
      "ownerId": 1,
      "timeZone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `availability` | array<object> |  |
| `id` | number |  |
| `isDefault` | boolean |  |
| `name` | string |  |
| `overrides` | array<object> |  |
| `ownerId` | number |  |
| `timeZone` | string |  |

## Native endpoint

Through the native Cal.com API, this operation is `GET /schedules` (base URL `https://api.cal.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-schedules.md) for the provider-specific parameters and requirements.

