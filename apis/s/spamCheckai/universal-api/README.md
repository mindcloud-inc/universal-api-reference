# <img src="https://images.mindcloud.co/apps/icons/spam-checkai_1774463215180.png" alt="SpamCheck.ai logo" width="28" height="28"> SpamCheck.ai: Universal API

SpamCheck.ai provides API-driven spam detection, email/IP validation, profanity checks, risky URL checks, language detection, and lead scoring for user-generated submissions.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/spamCheckai/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 4
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://spamcheck.ai
- **Vendor API docs:** https://app.spamcheck.ai/api_docs/index.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Spam Reports](actions/list-spam-reports.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/spamCheckai/latest/actions/list-spam-reports?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (4)

### Form Submissions

| Action | Method | Description |
| --- | --- | --- |
| [Check Submission for Spam](actions/check-submission-for-spam.md) | GET | Checks a submission for spam in SpamCheck.ai. |

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [Create Spam Report](actions/create-spam-report.md) | POST | Creates a new spam report in SpamCheck.ai. |
| [Delete Spam Report](actions/delete-spam-report.md) | DELETE | Deletes a spam report from SpamCheck.ai. |
| [List Spam Reports](actions/list-spam-reports.md) | GET | Retrieves saved spam reports from SpamCheck.ai. |

