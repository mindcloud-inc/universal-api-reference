# RotaCloud: Create Day Off

Creates days off in RotaCloud.

```
POST https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/create-day-off
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RotaCloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/create-day-off" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "dates[]": [
    {}
  ],
  "user": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/create-day-off', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "dates[]": [{}],
    "user": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `dates[]` | array<object> | yes | Array of day-off date objects. |
| `user` | number | yes | User ID for the day off. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dates": [
        {}
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
| `dates` | array<object> |  |
| `user` | number |  |

## Native endpoint

Through the native RotaCloud API, this operation is `POST /v1/days_off` (base URL `https://api.rotacloud.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-day-off.md) for the provider-specific parameters and requirements.

