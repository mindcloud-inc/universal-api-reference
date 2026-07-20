# Cal.com: Delete Reserved Slot

Deletes a reserved slot from Cal.com.

```
DELETE https://connect.mindcloud.co/v1/universal/cal/latest/actions/delete-reserved-slot
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cal.com `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/cal/latest/actions/delete-reserved-slot?connectionId=$CONNECTION_ID&uid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "uid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cal/latest/actions/delete-reserved-slot?${params}`, {
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
| `uid` | string | yes | Reservation UID from Cal.com path parameter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | string |  |

## Native endpoint

Through the native Cal.com API, this operation is `DELETE /slots/reservations/:uid` (base URL `https://api.cal.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-reserved-slot.md) for the provider-specific parameters and requirements.

