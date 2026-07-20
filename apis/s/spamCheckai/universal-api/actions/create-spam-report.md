# SpamCheck.ai: Create Spam Report

Creates a new spam report in SpamCheck.ai.

```
POST https://connect.mindcloud.co/v1/universal/spamCheckai/latest/actions/create-spam-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SpamCheck.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/spamCheckai/latest/actions/create-spam-report" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "body": {},
  "result": true,
  "desiredOutcome": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/spamCheckai/latest/actions/create-spam-report', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "body": {},
    "result": true,
    "desiredOutcome": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `body` | object | yes | JSON object containing the submission fields or message content recorded in the spam report. |
| `result` | boolean | yes | Whether the submission was classified as spam. |
| `desiredOutcome` | boolean | yes | The expected or desired spam classification for this report. |
| `ip` | string | no | IP address associated with the report. |
| `email` | string | no | Email address associated with the report. |
| `notes` | string | no | Optional notes for the spam report. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "admin_notes": "string",
      "admin_verified_at": "2026-05-07T12:00:00.000Z",
      "admin_verified_status": "string",
      "body": {},
      "created_at": "2026-05-07T12:00:00.000Z",
      "desired_outcome": true,
      "email": "ava@example.com",
      "external_metadata": {},
      "id": 1,
      "ip": "string",
      "notes": "string",
      "result": true,
      "updated_at": "2026-05-07T12:00:00.000Z",
      "user_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `admin_notes` | string |  |
| `admin_verified_at` | date |  |
| `admin_verified_status` | string |  |
| `body` | object |  |
| `created_at` | date |  |
| `desired_outcome` | boolean |  |
| `email` | string |  |
| `external_metadata` | object |  |
| `id` | number |  |
| `ip` | string |  |
| `notes` | string |  |
| `result` | boolean |  |
| `updated_at` | date |  |
| `user_id` | number |  |

## Native endpoint

Through the native SpamCheck.ai API, this operation is `POST /spam_reports` (base URL `https://api.spamcheck.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-spam-report.md) for the provider-specific parameters and requirements.

