# <img src="https://images.mindcloud.co/apps/icons/image-2839-vectorized_1777470940815.png" alt="AbcSubmit logo" width="28" height="28"> AbcSubmit: Universal API

Create forms, collect submissions, and automate workflows

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/abcSubmit/latest
- **Category:** Productivity / Forms & Surveys
- **Actions:** 16
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.abcsubmit.com/
- **Vendor API docs:** https://www.abcsubmit.com/site/api-documentation/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get My Plan](actions/get-my-plan.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/abcSubmit/latest/actions/get-my-plan?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (16)

### Authentication Response

| Action | Method | Description |
| --- | --- | --- |
| [Login](actions/login.md) | GET | Authenticates a user in AbcSubmit. |

### Form

| Action | Method | Description |
| --- | --- | --- |
| [Get Form Document](actions/get-form-document.md) | GET | Retrieves a form document from AbcSubmit. |
| [Get Form JS Embed Code](actions/get-form-js-embed-code.md) | GET | Retrieves JavaScript embed code for an AbcSubmit form. |
| [List Forms](actions/list-forms.md) | GET | Retrieves your forms from AbcSubmit. |

### Form Submission

| Action | Method | Description |
| --- | --- | --- |
| [Export Submissions](actions/export-submissions.md) | GET | Creates a submission export request for an AbcSubmit form. |
| [Get Submissions](actions/get-submissions.md) | GET | Retrieves submissions for an AbcSubmit form. |
| [Get Submissions Count](actions/get-submissions-count.md) | GET | Retrieves the submission count for an AbcSubmit form. |

### Plan

| Action | Method | Description |
| --- | --- | --- |
| [Get My Plan](actions/get-my-plan.md) | GET | Retrieves your current AbcSubmit plan limits. |

### Subscription Plan

| Action | Method | Description |
| --- | --- | --- |
| [Get My Upgrade Plans](actions/get-my-upgrade-plans.md) | GET | Retrieves your personalized upgrade plans from AbcSubmit. |
| [List Plans](actions/list-plans.md) | GET | Retrieves public subscription plans from AbcSubmit. |

### Template

| Action | Method | Description |
| --- | --- | --- |
| [Get Form Template Document](actions/get-form-template-document.md) | GET | Retrieves a form template document from AbcSubmit. |
| [List Form Templates](actions/list-form-templates.md) | GET | Retrieves form templates from AbcSubmit. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Change Password](actions/change-password.md) | PUT | Updates a user's password in AbcSubmit. |
| [Create Account](actions/create-account.md) | POST | Creates a new AbcSubmit account. |
| [Forgot Password](actions/forgot-password.md) | PUT | Requests an AbcSubmit password reset email. |
| [Get My Stats](actions/get-my-stats.md) | GET | Retrieves your current AbcSubmit plan usage. |

