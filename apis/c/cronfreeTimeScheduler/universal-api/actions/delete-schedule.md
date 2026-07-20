# Cronfree Time Scheduler: Delete Schedule

Deletes an existing schedule from Cronfree Time Scheduler.

```
DELETE https://connect.mindcloud.co/v1/universal/cronfreeTimeScheduler/latest/actions/delete-schedule
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cronfree Time Scheduler `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/cronfreeTimeScheduler/latest/actions/delete-schedule?connectionId=$CONNECTION_ID&hookUrl=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "hookUrl": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cronfreeTimeScheduler/latest/actions/delete-schedule?${params}`, {
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
| `hookUrl` | string | yes | The scheduled webhook URL to remove from Cronfree. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean |  |

## Native endpoint

Through the native Cronfree Time Scheduler API, this operation is `POST /unschedule` (base URL `https://login.cronfree.com/zapier`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-schedule.md) for the provider-specific parameters and requirements.

