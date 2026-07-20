# Perfit: List Account Activity



```
GET https://connect.mindcloud.co/v1/universal/perfit/latest/actions/list-account-activity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Perfit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/perfit/latest/actions/list-account-activity?connectionId=$CONNECTION_ID&account=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "account": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/perfit/latest/actions/list-account-activity?${params}`, {
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
| `account` | string | yes | Perfit account name. |
| `q` | string | no | Email address to filter activity. |
| `view` | string | no | Response format. |
| `filters.track_type` | string | no | Filter by event type. |
| `filters.timestamp.gtrel` | string | no | Relative start time like now-1h. |
| `filters.timestamp.gt` | date | no | Absolute start time in ISO-8601 format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "account": "string",
      "batch_id": "string",
      "custom_args": {},
      "day_of_week": 1,
      "domain": "string",
      "email": "ava@example.com",
      "hour_of_day": 1,
      "mail_id": "string",
      "mail_type": "string",
      "mta": "string",
      "sent_timestamp": "2026-05-07T12:00:00.000Z",
      "tags": [
        "string"
      ],
      "timestamp": "2026-05-07T12:00:00.000Z",
      "track_id": "string",
      "track_type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account` | string | Perfit account name. |
| `batch_id` | string | Batch identifier. |
| `custom_args` | object | Provider custom arguments object. |
| `day_of_week` | number | Day of week for the event timestamp. |
| `domain` | string | Recipient email domain. |
| `email` | string | Recipient email address. |
| `hour_of_day` | number | Hour of day for the event timestamp. |
| `mail_id` | string | Sent email identifier. |
| `mail_type` | string | Email type. |
| `mta` | string | Mail transfer host used for send. |
| `sent_timestamp` | date | Send time of the related email. |
| `tags` | array<string> | Associated tags. |
| `timestamp` | date | Event creation time. |
| `track_id` | string | Unique event identifier. |
| `track_type` | string | Perfit event type. |

## Native endpoint

Through the native Perfit API, this operation is `GET /:account/activity` (base URL `https://api.myperfit.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-account-activity.md) for the provider-specific parameters and requirements.

