# Create Spam Report with SpamCheck.ai

Creates a new spam report in SpamCheck.ai.

## Endpoint

- **Method:** `POST`
- **Path:** `/spam_reports`
- **Base URL:** `https://api.spamcheck.ai/api/v1`
- **Official documentation:** [Create Spam Report](https://app.spamcheck.ai/api_docs/index.html#/default/post_spam_reports)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `object` | yes | JSON object containing the submission fields or message content recorded in the spam report. |
| `result` | body | `boolean` | yes | Whether the submission was classified as spam. |
| `desired_outcome` | body | `boolean` | yes | The expected or desired spam classification for this report. |
| `ip` | body | `string` | no | IP address associated with the report. |
| `email` | body | `string` | no | Email address associated with the report. |
| `notes` | body | `string` | no | Optional notes for the spam report. |
