# Cronfree Time Scheduler: Create Schedule

Creates a new schedule in Cronfree Time Scheduler.

```
POST https://connect.mindcloud.co/v1/universal/cronfreeTimeScheduler/latest/actions/create-schedule
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cronfree Time Scheduler `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cronfreeTimeScheduler/latest/actions/create-schedule" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "hookUrl": "https://example.com",
  "wdays[]": [
    "string"
  ],
  "months[]": [
    "string"
  ],
  "mdays[]": [
    "string"
  ],
  "hours[]": [
    "string"
  ],
  "minutes[]": [
    "string"
  ],
  "timezone": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cronfreeTimeScheduler/latest/actions/create-schedule', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "hookUrl": "https://example.com",
    "wdays[]": ["string"],
    "months[]": ["string"],
    "mdays[]": ["string"],
    "hours[]": ["string"],
    "minutes[]": ["string"],
    "timezone": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `hookUrl` | string | yes | The URL that Cronfree will POST to at the scheduled interval. |
| `wdays[]` | array<string> | yes |  |
| `months[]` | array<string> | yes |  |
| `mdays[]` | array<string> | yes |  |
| `hours[]` | array<string> | yes |  |
| `minutes[]` | array<string> | yes |  |
| `timezone` | string | yes |  |

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

Through the native Cronfree Time Scheduler API, this operation is `POST /schedule` (base URL `https://login.cronfree.com/zapier`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-schedule.md) for the provider-specific parameters and requirements.

