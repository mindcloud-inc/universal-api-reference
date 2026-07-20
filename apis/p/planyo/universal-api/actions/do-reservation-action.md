# Planyo: Do Reservation Action

Performs a reservation action in Planyo.

```
PUT https://connect.mindcloud.co/v1/universal/planyo/latest/actions/do-reservation-action
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Planyo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/planyo/latest/actions/do-reservation-action" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "reservationId": 1,
  "action": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/planyo/latest/actions/do-reservation-action', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "reservationId": 1,
    "action": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `reservationId` | number | yes |  |
| `action` | string | yes |  |
| `customData` | string | no |  |
| `comment` | string | no |  |
| `adminId` | number | no |  |
| `isQuiet` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": 1,
      "userText": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | number |  |
| `userText` | string |  |

## Native endpoint

Through the native Planyo API, this operation is `GET /` (base URL `https://www.planyo.com/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/do-reservation-action.md) for the provider-specific parameters and requirements.

