# <img src="https://images.mindcloud.co/apps/icons/survey-methods-icon_1777319518600.jpeg" alt="SurveyMethods logo" width="28" height="28"> SurveyMethods: Universal API

SurveyMethods is an online survey platform for creating surveys, collecting responses, managing contacts and groups, and automating survey workflows through its REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/surveyMethods/latest
- **Actions:** 18
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://surveymethods.com
- **Vendor API docs:** https://surveymethods.com/images/pdfs/surveymethodsapidocumentv1.pdf

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Surveys](actions/list-surveys.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/surveyMethods/latest/actions/list-surveys?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (18)

### Completed Response Summary

| Action | Method | Description |
| --- | --- | --- |
| [List Completed Response Summaries](actions/list-completed-response-summaries.md) | GET |  |

### Email List

| Action | Method | Description |
| --- | --- | --- |
| [List Email Lists](actions/list-email-lists.md) | GET |  |

### Email List Contact

| Action | Method | Description |
| --- | --- | --- |
| [List Email List Contacts](actions/list-email-list-contacts.md) | GET |  |

### Email Response Summary

| Action | Method | Description |
| --- | --- | --- |
| [List Email Response Summaries](actions/list-email-response-summaries.md) | GET |  |

### Master Opt-out Email

| Action | Method | Description |
| --- | --- | --- |
| [List Master Opt-Out Emails](actions/list-master-opt-out-emails.md) | GET |  |

### Newsletter Code

| Action | Method | Description |
| --- | --- | --- |
| [List Newsletter Codes](actions/list-newsletter-codes.md) | GET |  |

### Partial Response Summary

| Action | Method | Description |
| --- | --- | --- |
| [List Partial Response Summaries](actions/list-partial-response-summaries.md) | GET |  |

### Response

| Action | Method | Description |
| --- | --- | --- |
| [Get Response](actions/get-response.md) | GET |  |

### Response Code

| Action | Method | Description |
| --- | --- | --- |
| [List Response Codes](actions/list-response-codes.md) | GET |  |

### Response Dashboard

| Action | Method | Description |
| --- | --- | --- |
| [Get Response Dashboard](actions/get-response-dashboard.md) | GET |  |

### Response Question

| Action | Method | Description |
| --- | --- | --- |
| [Get Response Question](actions/get-response-question.md) | GET |  |

### Response Summary

| Action | Method | Description |
| --- | --- | --- |
| [List Response Summaries](actions/list-response-summaries.md) | GET |  |

### Survey

| Action | Method | Description |
| --- | --- | --- |
| [Get Survey](actions/get-survey.md) | GET |  |
| [List Surveys](actions/list-surveys.md) | GET |  |

### Survey Code

| Action | Method | Description |
| --- | --- | --- |
| [List Survey Codes](actions/list-survey-codes.md) | GET |  |

### User Details

| Action | Method | Description |
| --- | --- | --- |
| [Get User Details](actions/get-user-details.md) | GET |  |

### User Validation

| Action | Method | Description |
| --- | --- | --- |
| [Validate User](actions/validate-user.md) | GET |  |

### Web Response Summary

| Action | Method | Description |
| --- | --- | --- |
| [List Web Response Summaries](actions/list-web-response-summaries.md) | GET |  |

