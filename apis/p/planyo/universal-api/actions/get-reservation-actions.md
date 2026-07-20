# Planyo: Get Reservation Actions

Retrieves reservation actions from Planyo.

```
GET https://connect.mindcloud.co/v1/universal/planyo/latest/actions/get-reservation-actions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Planyo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/planyo/latest/actions/get-reservation-actions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/planyo/latest/actions/get-reservation-actions?${params}`, {
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
| `reservationId` | number | no |  |
| `userId` | number | no |  |
| `startTime` | string | no |  |
| `endTime` | string | no |  |
| `eventType` | number | no |  |
| `siteId` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "results": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `results` | array<object> |  |

## Native endpoint

Through the native Planyo API, this operation is `GET /` (base URL `https://www.planyo.com/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-reservation-actions.md) for the provider-specific parameters and requirements.

