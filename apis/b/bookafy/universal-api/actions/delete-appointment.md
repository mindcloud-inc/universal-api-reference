# Bookafy: Delete Appointment

Deletes or cancels an appointment in Bookafy.

```
DELETE https://connect.mindcloud.co/v1/universal/bookafy/latest/actions/delete-appointment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bookafy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/bookafy/latest/actions/delete-appointment?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bookafy/latest/actions/delete-appointment?${params}`, {
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
| `id` | string | no | Bookafy appointment ID to cancel. |
| `userId` | string | no | Bookafy staff user ID that owns the appointment. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": {
        "message": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response.message` | string | Bookafy status message for the cancel request. |

## Native endpoint

Through the native Bookafy API, this operation is `DELETE /appointments/:id` (base URL `https://app.bookafy.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-appointment.md) for the provider-specific parameters and requirements.

