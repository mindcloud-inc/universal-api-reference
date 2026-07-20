# <img src="https://images.mindcloud.co/apps/icons/nicereply_1775768651684.png" alt="Nicereply logo" width="28" height="28"> Nicereply: Universal API

Collect feedback, run surveys, and analyze customer experience

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/nicereply/latest
- **Category:** Productivity / Forms & Surveys
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.nicereply.com
- **Vendor API docs:** https://cdn.nicereply.com/s/api/latest/reference/introduction/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Rating Values Settings](actions/get-rating-values-settings.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nicereply/latest/actions/get-rating-values-settings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Customer

| Action | Method | Description |
| --- | --- | --- |
| [Get Customer](actions/get-customer.md) | GET | Retrieves details for a customer from Nicereply. |
| [List Customers](actions/list-customers.md) | GET | Retrieves a list of customers from Nicereply. |

### Feedback Object

| Action | Method | Description |
| --- | --- | --- |
| [Create Feedback Object](actions/create-feedback-object.md) | POST | Creates a feedback object in Nicereply. |
| [Get Feedback Object](actions/get-feedback-object.md) | GET | Retrieves a feedback object from Nicereply. |
| [List Feedback Objects](actions/list-feedback-objects.md) | GET | Retrieves a list of feedback objects from Nicereply. |

### Feedback Object Group

| Action | Method | Description |
| --- | --- | --- |
| [Get Feedback Object Group](actions/get-feedback-object-group.md) | GET | Retrieves a feedback object group from Nicereply. |
| [List Feedback Object Groups](actions/list-feedback-object-groups.md) | GET | Retrieves feedback object groups from Nicereply. |

### Integration

| Action | Method | Description |
| --- | --- | --- |
| [List Integrations](actions/list-integrations.md) | GET | Retrieves a list of integrations from Nicereply. |

### Rating Values

| Action | Method | Description |
| --- | --- | --- |
| [Get Rating Values Settings](actions/get-rating-values-settings.md) | GET | Retrieves rating value settings from Nicereply. |

### Response

| Action | Method | Description |
| --- | --- | --- |
| [Create Response](actions/create-response.md) | POST | Creates a new response in Nicereply. |
| [Get Response](actions/get-response.md) | GET | Retrieves details for a response from Nicereply. |
| [List Feedback Object Group Responses](actions/list-feedback-object-group-responses.md) | GET | Retrieves responses for a feedback object group in Nicereply. |
| [List Feedback Object Responses](actions/list-feedback-object-responses.md) | GET | Retrieves responses for a feedback object in Nicereply. |
| [List Responses](actions/list-responses.md) | GET | Retrieves a list of responses from Nicereply. |
| [List Survey Responses](actions/list-survey-responses.md) | GET | Retrieves responses for a survey in Nicereply. |
| [Update Response Feedback Object](actions/update-response-feedback-object.md) | PUT | Updates a response's feedback object in Nicereply. |

### Response Issue Status

| Action | Method | Description |
| --- | --- | --- |
| [Get Response Issue Status](actions/get-response-issue-status.md) | GET | Retrieves a response issue status from Nicereply. |
| [Ignore Response Issue Status](actions/ignore-response-issue-status.md) | PUT | Ignores a response issue in Nicereply. |
| [Resolve Response Issue Status](actions/resolve-response-issue-status.md) | PUT | Resolves a response issue in Nicereply. |

### Response Tag

| Action | Method | Description |
| --- | --- | --- |
| [Assign Response Tags](actions/assign-response-tags.md) | PUT | Assigns a tag to a response in Nicereply. |
| [Unassign Response Tags](actions/unassign-response-tags.md) | DELETE | Unassigns a tag from a response in Nicereply. |

### Survey

| Action | Method | Description |
| --- | --- | --- |
| [Get Survey](actions/get-survey.md) | GET | Retrieves details for a survey from Nicereply. |
| [List Surveys](actions/list-surveys.md) | GET | Retrieves a list of surveys from Nicereply. |

### Survey Distribution

| Action | Method | Description |
| --- | --- | --- |
| [View Survey Distribution](actions/view-survey-distribution.md) | GET | Retrieves survey distribution settings from Nicereply. |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [Create Tag](actions/create-tag.md) | POST | Creates a new tag in Nicereply. |
| [Get Tag](actions/get-tag.md) | GET | Retrieves details for a tag from Nicereply. |
| [List Tags](actions/list-tags.md) | GET | Retrieves a list of tags from Nicereply. |

### Ticket Link

| Action | Method | Description |
| --- | --- | --- |
| [Get Response Ticket Link](actions/get-response-ticket-link.md) | GET | Retrieves a response ticket link from Nicereply. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get User](actions/get-user.md) | GET | Retrieves details for a user from Nicereply. |
| [List Users](actions/list-users.md) | GET | Retrieves a list of users from Nicereply. |

