# Tailwind: List Timeslots

Retrieves publishing timeslots from Tailwind.

```
GET https://connect.mindcloud.co/v1/universal/tailwind/latest/actions/list-timeslots
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tailwind `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tailwind/latest/actions/list-timeslots?connectionId=$CONNECTION_ID&accountId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tailwind/latest/actions/list-timeslots?${params}`, {
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
| `accountId` | string | yes | Pinterest account ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": "string",
      "dayPreference": 1,
      "id": "string",
      "sendAt": 1,
      "timePreference": "string",
      "timezone": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | string | Pinterest account ID. |
| `dayPreference` | number | Day of week where 0 is Sunday. |
| `id` | string | Timeslot ID. |
| `sendAt` | number | Unix timestamp of the next scheduled send. |
| `timePreference` | string | Preferred time in HH:MM format. |
| `timezone` | string | Timezone name. |
| `type` | string | Timeslot type. |

## Native endpoint

Through the native Tailwind API, this operation is `GET /v1/accounts/:accountId/timeslots` (base URL `https://api-v1.tailwind.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-timeslots.md) for the provider-specific parameters and requirements.

