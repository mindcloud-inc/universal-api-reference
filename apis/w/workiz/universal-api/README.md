# <img src="https://images.mindcloud.co/apps/icons/workiz_1773347526316.png" alt="Workiz logo" width="28" height="28"> Workiz: Universal API

Schedule jobs, dispatch teams, invoice customers, and manage leads

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/workiz/latest
- **Category:** Support / Field Service
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.workiz.com/
- **Vendor API docs:** https://developer.workiz.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Team Members](actions/list-team-members.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/workiz/latest/actions/list-team-members?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Jobs

| Action | Method | Description |
| --- | --- | --- |
| [Add Job Payment](actions/add-job-payment.md) | PUT | Adds a payment to a job in Workiz. |
| [Assign User to Job](actions/assign-user-to-job.md) | PUT | Assigns a user to a job in Workiz. |
| [Create Job](actions/create-job.md) | POST | Creates a new job in Workiz. |
| [Get Job](actions/get-job.md) | GET | Retrieves a job from Workiz by UUID. |
| [List Jobs](actions/list-jobs.md) | GET | Finds jobs in Workiz by filter criteria. |
| [Unassign User from Job](actions/unassign-user-from-job.md) | PUT | Unassigns a user from a job in Workiz. |
| [Update Job](actions/update-job.md) | PUT | Updates an existing job in Workiz. |

### Leads

| Action | Method | Description |
| --- | --- | --- |
| [Activate Lead](actions/activate-lead.md) | PUT | Activates an existing lead in Workiz. |
| [Assign User to Lead](actions/assign-user-to-lead.md) | PUT | Assigns a user to a lead in Workiz. |
| [Convert Lead To Job](actions/convert-lead-to-job.md) | PUT | Converts a lead to a job in Workiz. |
| [Create Lead](actions/create-lead.md) | POST | Creates a new lead in Workiz. |
| [Get Lead](actions/get-lead.md) | GET | Retrieves a lead from Workiz by UUID. |
| [List Leads](actions/list-leads.md) | GET | Finds leads in Workiz by filter criteria. |
| [Mark Lead Lost](actions/mark-lead-lost.md) | PUT | Marks an existing lead as lost in Workiz. |
| [Unassign User from Lead](actions/unassign-user-from-lead.md) | PUT | Unassigns a user from a lead in Workiz. |
| [Update Lead](actions/update-lead.md) | PUT | Updates an existing lead in Workiz. |

### Teams

| Action | Method | Description |
| --- | --- | --- |
| [Get Team Member](actions/get-team-member.md) | GET | Retrieves a team member from Workiz by user ID. |
| [List Team Members](actions/list-team-members.md) | GET | Finds all team members in Workiz. |

### Time Off

| Action | Method | Description |
| --- | --- | --- |
| [List Time Offs](actions/list-time-offs.md) | GET | Finds time off entries in Workiz. |
| [List Time Offs by User](actions/list-time-offs-by-user.md) | GET | Finds time off entries in Workiz by user name. |

