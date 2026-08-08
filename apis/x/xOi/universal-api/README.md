# <img src="https://images.mindcloud.co/apps/icons/x-oi_1786031804983.png" alt="XOi logo" width="28" height="28"> XOi: Universal API

Connect XOi Vision to manage jobs, content, users, shares, and Live calls.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/xOi/latest
- **Category:** Support / Field Service
- **Actions:** 31
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://xoi.io/
- **Vendor API docs:** https://integration-docs.xoi.io/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Content](actions/get-content.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xOi/latest/actions/get-content?connectionId=$CONNECTION_ID&contentIds%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (31)

### Content

| Action | Method | Description |
| --- | --- | --- |
| [Get Content](actions/get-content.md) | GET |  |

### Content Media Url

| Action | Method | Description |
| --- | --- | --- |
| [Get Content Media URLs](actions/get-content-media-urls.md) | GET |  |

### Documentation

| Action | Method | Description |
| --- | --- | --- |
| [List Documentation](actions/list-documentation.md) | GET |  |
| [List Documentation by Date Range](actions/list-documentation-by-date-range.md) | GET |  |

### Group

| Action | Method | Description |
| --- | --- | --- |
| [Get Groups](actions/get-groups.md) | GET |  |

### Job

| Action | Method | Description |
| --- | --- | --- |
| [Create Job](actions/create-job.md) | POST |  |
| [Delete Job](actions/delete-job.md) | DELETE |  |
| [Get Job](actions/get-job.md) | GET |  |
| [Get Job ID by External ID](actions/get-job-id-by-external-id.md) | GET |  |
| [Get Job IDs](actions/get-job-ids.md) | GET |  |
| [List Jobs](actions/list-jobs.md) | GET |  |
| [List Jobs by Customer Name](actions/list-jobs-by-customer-name.md) | GET |  |
| [List Jobs by Date Range](actions/list-jobs-by-date-range.md) | GET |  |
| [List Jobs by Job Location](actions/list-jobs-by-job-location.md) | GET |  |
| [List Jobs by Work Order](actions/list-jobs-by-work-order.md) | GET |  |
| [Update Job](actions/update-job.md) | PUT |  |

### Job Summary

| Action | Method | Description |
| --- | --- | --- |
| [Get Job Summary](actions/get-job-summary.md) | GET |  |
| [Get Workflow Job Summary](actions/get-workflow-job-summary.md) | GET |  |

### Knowledge Base Content

| Action | Method | Description |
| --- | --- | --- |
| [Search Knowledge Base](actions/search-knowledge-base.md) | GET |  |

### Live Call

| Action | Method | Description |
| --- | --- | --- |
| [Get Live Call Data](actions/get-live-call-data.md) | GET |  |
| [Prepare Live Call](actions/prepare-live-call.md) | POST |  |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Authenticate](actions/authenticate.md) | POST |  |

### Share Link

| Action | Method | Description |
| --- | --- | --- |
| [Create Knowledge Base Share Link](actions/create-knowledge-base-share-link.md) | POST |  |
| [Create Multi-Job Share Link](actions/create-multi-job-share-link.md) | POST |  |
| [Create Share Link](actions/create-share-link.md) | POST |  |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get User](actions/get-user.md) | GET |  |
| [Get Users by Email](actions/get-users-by-email.md) | GET |  |
| [List Users](actions/list-users.md) | GET |  |

### Webhook Event

| Action | Method | Description |
| --- | --- | --- |
| [List Content Webhook History](actions/list-content-webhook-history.md) | GET |  |
| [List Jobs Webhook History](actions/list-jobs-webhook-history.md) | GET |  |

### Workflow Reporting Data

| Action | Method | Description |
| --- | --- | --- |
| [Get Workflow Reporting Data](actions/get-workflow-reporting-data.md) | GET |  |

