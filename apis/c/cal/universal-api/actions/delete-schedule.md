# Cal.com: Delete Schedule

Deletes a schedule from Cal.com.

```
DELETE https://connect.mindcloud.co/v1/universal/cal/latest/actions/delete-schedule
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cal.com `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/cal/latest/actions/delete-schedule?connectionId=$CONNECTION_ID&scheduleId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "scheduleId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cal/latest/actions/delete-schedule?${params}`, {
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
| `scheduleId` | list | yes | Schedule identifier from Cal.com path parameter. |

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

Through the native Cal.com API, this operation is `DELETE /schedules/:scheduleId` (base URL `https://api.cal.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-schedule.md) for the provider-specific parameters and requirements.

