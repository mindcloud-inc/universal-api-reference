# Check Submission for Spam with SpamCheck.ai

Checks a submission for spam in SpamCheck.ai.

## Endpoint

- **Method:** `POST`
- **Path:** `/spam/check`
- **Base URL:** `https://api.spamcheck.ai/api/v1`
- **Official documentation:** [Check Submission for Spam](https://app.spamcheck.ai/api_docs/index.html#/default/post_spam_check)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `object` | yes | JSON object containing the submission fields or message content to evaluate for spam. |
| `ip` | body | `string` | no | IP address associated with the submission. |
| `email` | body | `string` | no | Email address associated with the submission. |
| `email_validation_method` | body | `string` | no | SpamCheck.ai email validation method. Use mx or smtp. |
| `context` | body | `string` | no | Optional context to help interpret the submission. |
| `score_threshold` | body | `number` | no | Optional score threshold from 0 to 100. |
