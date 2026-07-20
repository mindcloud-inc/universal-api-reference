# <img src="https://images.mindcloud.co/apps/icons/service-m8_1773170948302.png" alt="ServiceM8 logo" width="28" height="28"> ServiceM8: Universal API

Manage field service jobs, clients, staff, and job templates

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/serviceM8/latest
- **Category:** Support / Field Service
- **Actions:** 22
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.servicem8.com/
- **Vendor API docs:** https://developer.servicem8.com/docs/rest-overview

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Clients](actions/list-clients.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/serviceM8/latest/actions/list-clients?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (22)

### Client

| Action | Method | Description |
| --- | --- | --- |
| [Create Client](actions/create-client.md) | POST |  |
| [Get Client](actions/get-client.md) | GET |  |
| [List Clients](actions/list-clients.md) | GET |  |
| [Update Client](actions/update-client.md) | PUT |  |

### Company Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Company Contact](actions/create-company-contact.md) | POST |  |
| [List Company Contacts](actions/list-company-contacts.md) | GET |  |
| [Update Company Contact](actions/update-company-contact.md) | PUT |  |

### Job

| Action | Method | Description |
| --- | --- | --- |
| [Create Job](actions/create-job.md) | POST |  |
| [Get Job](actions/get-job.md) | GET |  |
| [List Jobs](actions/list-jobs.md) | GET |  |
| [Update Job](actions/update-job.md) | PUT |  |

### Job Activity

| Action | Method | Description |
| --- | --- | --- |
| [Create Job Activity](actions/create-job-activity.md) | POST |  |
| [List Job Activities](actions/list-job-activities.md) | GET |  |
| [Update Job Activity](actions/update-job-activity.md) | PUT |  |

### Job Allocation

| Action | Method | Description |
| --- | --- | --- |
| [Create Job Allocation](actions/create-job-allocation.md) | POST |  |
| [List Job Allocations](actions/list-job-allocations.md) | GET |  |

### Staff Member

| Action | Method | Description |
| --- | --- | --- |
| [Get Staff Member](actions/get-staff-member.md) | GET |  |
| [List Staff Members](actions/list-staff-members.md) | GET |  |
| [Update Staff Member](actions/update-staff-member.md) | PUT |  |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [Create Task](actions/create-task.md) | POST |  |
| [List Tasks](actions/list-tasks.md) | GET |  |
| [Update Task](actions/update-task.md) | PUT |  |

