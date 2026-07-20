# Zubie: Create Schedule

Creates a schedule in Zubie.

```
POST https://connect.mindcloud.co/v1/universal/zubie/latest/actions/create-schedule
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zubie `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zubie/latest/actions/create-schedule" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "periods[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zubie/latest/actions/create-schedule', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "periods[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `periods[]` | array<object> | yes | List of schedule periods. |

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

Through the native Zubie API, this operation is `POST /schedules` (base URL `https://api.zubiecar.com/api/v2/zinc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-schedule.md) for the provider-specific parameters and requirements.

