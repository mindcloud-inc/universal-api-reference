# <img src="https://images.mindcloud.co/apps/icons/id-cxyms9sm-logos_1775150809560.png" alt="CodeSubmit logo" width="28" height="28"> CodeSubmit: Universal API

Create assessments, invite candidates, and track interview results

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/codeSubmit/latest
- **Category:** Human Resources / Recruiting
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.codesubmit.io
- **Vendor API docs:** https://www.codesubmit.io/integrations/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/codeSubmit/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Candidates

| Action | Method | Description |
| --- | --- | --- |
| [Invite Candidate](actions/invite-candidate.md) | POST |  |
| [List Candidates](actions/list-candidates.md) | GET |  |

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [Get Company Settings](actions/get-company-settings.md) | GET |  |
| [Update Company](actions/update-company.md) | PUT |  |
| [Update Company Settings](actions/update-company-settings.md) | PUT |  |

### Customers

| Action | Method | Description |
| --- | --- | --- |
| [Get Billing Customer](actions/get-billing-customer.md) | GET |  |

### Invoices

| Action | Method | Description |
| --- | --- | --- |
| [List Invoices](actions/list-invoices.md) | GET |  |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Create Integration](actions/create-integration.md) | POST |  |
| [Create Talent Boost](actions/create-talent-boost.md) | POST |  |
| [Create Talent Job](actions/create-talent-job.md) | POST |  |
| [Delete Integration](actions/delete-integration.md) | DELETE |  |
| [Get Talent Settings](actions/get-talent-settings.md) | GET |  |
| [List Integrations](actions/list-integrations.md) | GET |  |
| [List Talent Jobs](actions/list-talent-jobs.md) | GET |  |
| [Open Billing Portal](actions/open-billing-portal.md) | POST |  |
| [Update Integration](actions/update-integration.md) | PUT |  |
| [Update Talent Settings](actions/update-talent-settings.md) | PUT |  |

### Subscriptions

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Subscription](actions/cancel-subscription.md) | DELETE |  |
| [Get Subscription](actions/get-subscription.md) | GET |  |
| [Update Subscription](actions/update-subscription.md) | PUT |  |

### Templates

| Action | Method | Description |
| --- | --- | --- |
| [Create CodePair Template](actions/create-code-pair-template.md) | POST |  |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Change My Password](actions/change-my-password.md) | PUT |  |
| [Create Assessment](actions/create-assessment.md) | POST |  |
| [Create Bytes Assessment](actions/create-bytes-assessment.md) | POST |  |
| [Create CodePair Session](actions/create-code-pair-session.md) | POST |  |
| [Get Applicants Stats](actions/get-applicants-stats.md) | GET |  |
| [Get Candidate Invite Trend](actions/get-candidate-invite-trend.md) | GET |  |
| [Get Candidates Completed Stats](actions/get-candidates-completed-stats.md) | GET |  |
| [Get Candidates Invited Stats](actions/get-candidates-invited-stats.md) | GET |  |
| [Get My Settings](actions/get-my-settings.md) | GET |  |
| [List Assessments](actions/list-assessments.md) | GET |  |
| [List Library Challenges](actions/list-library-challenges.md) | GET |  |
| [List Quick Create Languages](actions/list-quick-create-languages.md) | GET |  |
| [Quick Create CodePair](actions/quick-create-code-pair.md) | POST |  |
| [Request Library Challenge](actions/request-library-challenge.md) | POST |  |
| [Update My Settings](actions/update-my-settings.md) | PUT |  |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Invite Users](actions/bulk-invite-users.md) | POST |  |
| [Get Current User](actions/get-current-user.md) | GET |  |
| [Invite Company User](actions/invite-company-user.md) | POST |  |
| [List Company Users](actions/list-company-users.md) | GET |  |

