# SpamCheck.ai: Check Submission for Spam

Checks a submission for spam in SpamCheck.ai.

```
GET https://connect.mindcloud.co/v1/universal/spamCheckai/latest/actions/check-submission-for-spam
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SpamCheck.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/spamCheckai/latest/actions/check-submission-for-spam?connectionId=$CONNECTION_ID&body=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "body": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/spamCheckai/latest/actions/check-submission-for-spam?${params}`, {
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
| `body` | object | yes | JSON object containing the submission fields or message content to evaluate for spam. |
| `ip` | string | no | IP address associated with the submission. |
| `email` | string | no | Email address associated with the submission. |
| `emailValidationMethod` | string | no | SpamCheck.ai email validation method. Use mx or smtp. |
| `context` | string | no | Optional context to help interpret the submission. |
| `scoreThreshold` | number | no | Optional score threshold from 0 to 100. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": {
        "language": {
          "data": [
            [
              "string"
            ]
          ]
        },
        "profanity": {
          "data": {},
          "result": true
        },
        "redirect_urls": {
          "result": true
        },
        "risky_urls": {
          "data": [
            {}
          ],
          "result": true
        },
        "short_urls": {
          "result": true
        },
        "spam": {
          "data": {
            "score": 1
          },
          "result": true
        }
      },
      "email": {
        "blocked": {
          "result": true
        },
        "mx_valid": {
          "result": true
        },
        "regex_valid": {
          "result": true
        },
        "smtp_valid": {
          "result": true
        }
      },
      "id": 1,
      "ip": {
        "blocked": {
          "result": true
        }
      },
      "mark_as_incorrect": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content.language.data` | array<array> |  |
| `content.profanity.data` | object |  |
| `content.profanity.result` | boolean |  |
| `content.redirect_urls.result` | boolean |  |
| `content.risky_urls.data` | array<object> |  |
| `content.risky_urls.result` | boolean |  |
| `content.short_urls.result` | boolean |  |
| `content.spam.data.score` | number |  |
| `content.spam.result` | boolean |  |
| `email.blocked.result` | boolean |  |
| `email.mx_valid.result` | boolean |  |
| `email.regex_valid.result` | boolean |  |
| `email.smtp_valid.result` | boolean |  |
| `id` | number |  |
| `ip.blocked.result` | boolean |  |
| `mark_as_incorrect` | string |  |

## Native endpoint

Through the native SpamCheck.ai API, this operation is `POST /spam/check` (base URL `https://api.spamcheck.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-submission-for-spam.md) for the provider-specific parameters and requirements.

