# <img src="https://images.mindcloud.co/apps/icons/retently_1773931160351.png" alt="Retently logo" width="28" height="28"> Retently: Universal API

Manage customers, campaigns, surveys, and NPS feedback

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/retently/latest
- **Category:** Marketing
- **Actions:** 25
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.retently.com
- **Vendor API docs:** https://www.retently.com/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Customers](actions/list-customers.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/retently/latest/actions/list-customers?connectionId=$CONNECTION_ID&limit=25&offset=0&attributes%5B%5D.name=Ava%20Chen&attributes%5B%5D.op=string&attributes%5B%5D.value=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (25)

### Campaigns

| Action | Method | Description |
| --- | --- | --- |
| [List Campaign Reports](actions/list-campaign-reports.md) | GET | Retrieves a list of campaign reports from Retently. |
| [List Campaigns](actions/list-campaigns.md) | GET | Retrieves a list of campaigns from Retently. |

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [Get Company](actions/get-company.md) | GET | Retrieves a company from Retently by ID or domain. |
| [List Companies](actions/list-companies.md) | GET | Retrieves a list of companies from Retently. |

### Customers

| Action | Method | Description |
| --- | --- | --- |
| [Delete Customers](actions/delete-customers.md) | DELETE | Deletes existing customer records from Retently. |
| [Get Customer](actions/get-customer.md) | GET | Retrieves a customer from Retently by ID. |
| [List Customers](actions/list-customers.md) | GET | Retrieves a list of customers from Retently. |
| [Unsubscribe Customers](actions/unsubscribe-customers.md) | PUT | Unsubscribes customers from surveys in Retently. |
| [Upsert Customers](actions/upsert-customers.md) | PUT | Creates or updates customers in Retently. |

### Email Templates

| Action | Method | Description |
| --- | --- | --- |
| [List Templates](actions/list-templates.md) | GET | Retrieves a list of email templates from Retently. |

### Emails

| Action | Method | Description |
| --- | --- | --- |
| [Add Suppressed Email](actions/add-suppressed-email.md) | POST | Creates a suppressed email entry in Retently. |
| [List Suppressed Emails](actions/list-suppressed-emails.md) | GET | Retrieves a list of suppressed emails from Retently. |
| [Remove Suppressed Email](actions/remove-suppressed-email.md) | DELETE | Deletes a suppressed email entry from Retently. |

### Groups

| Action | Method | Description |
| --- | --- | --- |
| [Get Group Trends](actions/get-group-trends.md) | GET | Retrieves trend data for a group from Retently. |
| [List Trend Groups](actions/list-trend-groups.md) | GET | Retrieves a list of trend groups from Retently. |

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [List Outbox](actions/list-outbox.md) | GET | Retrieves a list of sent surveys from Retently. |
| [Send Transactional Survey](actions/send-transactional-survey.md) | POST | Sends a transactional survey through Retently. |

### Metrics

| Action | Method | Description |
| --- | --- | --- |
| [Get Latest Score](actions/get-latest-score.md) | GET | Retrieves the latest metric score from Retently. |

### Satisfaction Responses

| Action | Method | Description |
| --- | --- | --- |
| [Add Feedback Tags](actions/add-feedback-tags.md) | PUT | Updates tags on a feedback response in Retently. |
| [Add Feedback Topics](actions/add-feedback-topics.md) | PUT | Updates topics on a feedback response in Retently. |
| [Get Feedback](actions/get-feedback.md) | GET | Retrieves a feedback response from Retently by ID. |
| [List Feedback](actions/list-feedback.md) | GET | Retrieves a list of feedback responses from Retently. |

### Suppressed Domain

| Action | Method | Description |
| --- | --- | --- |
| [Add Suppressed Domain](actions/add-suppressed-domain.md) | POST | Creates a suppressed domain entry in Retently. |
| [List Suppressed Domains](actions/list-suppressed-domains.md) | GET | Retrieves a list of suppressed domains from Retently. |
| [Remove Suppressed Domain](actions/remove-suppressed-domain.md) | DELETE | Deletes a suppressed domain entry from Retently. |

