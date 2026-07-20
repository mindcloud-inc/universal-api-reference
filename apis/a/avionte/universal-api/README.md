# <img src="https://images.mindcloud.co/apps/icons/avionte_1777387293287.png" alt="Avionte logo" width="28" height="28"> Avionte: Universal API

The only true end-to-end staffing and recruiting software in one single platform

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/avionte/latest
- **Category:** Human Resources / Recruiting
- **Actions:** 33
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.avionte.com
- **Vendor API docs:** https://developer.avionte.com/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Branches](actions/get-branches.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/avionte/latest/actions/get-branches?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (33)

### Branches

| Action | Method | Description |
| --- | --- | --- |
| [Get Branches](actions/get-branches.md) | GET | Retrieves branches from Avionte. |

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [Get a Company](actions/get-a-company.md) | GET | Retrieves a company from Avionte. |
| [Get Company IDs](actions/get-company-ids.md) | GET | Retrieves company IDs from Avionte. |

### Jobs

| Action | Method | Description |
| --- | --- | --- |
| [Get a Job](actions/get-a-job.md) | GET | Retrieves a job from Avionte. |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Add Talent to Pipeline Stage](actions/add-talent-to-pipeline-stage.md) | POST |  |
| [Create Talent Activity](actions/create-talent-activity.md) | POST |  |
| [Create Talent Tag](actions/create-talent-tag.md) | POST |  |
| [Get a Contact](actions/get-a-contact.md) | GET | Retrieves a contact from Avionte. |
| [Get a Department](actions/get-a-department.md) | GET | Retrieves a department from Avionte. |
| [Get a List of Talent Assessments](actions/get-a-list-of-talent-assessments.md) | GET | Retrieves talent assessments from Avionte. |
| [Get a Placement](actions/get-a-placement.md) | GET | Retrieves a placement from Avionte. |
| [Get a Talent Nomination Stage](actions/get-a-talent-nomination-stage.md) | GET |  |
| [Get Applicant Posted Jobs](actions/get-applicant-posted-jobs.md) | GET | Retrieves posted jobs for a talent from Avionte. |
| [Get Available Talent Statuses](actions/get-available-talent-statuses.md) | GET | Retrieves talent statuses from Avionte. |
| [Get Certificates](actions/get-certificates.md) | GET | Retrieves certificates from Avionte. |
| [Get Contact IDs](actions/get-contact-ids.md) | GET | Retrieves contact IDs from Avionte. |
| [Get Department IDs](actions/get-department-ids.md) | GET | Retrieves department IDs from Avionte. |
| [Get Job IDs](actions/get-job-ids.md) | GET |  |
| [Get Placement IDs](actions/get-placement-ids.md) | GET | Retrieves placement IDs from Avionte. |
| [Get Skill Positions](actions/get-skill-positions.md) | GET | Retrieves skill positions from Avionte. |
| [Get Talent Document Types](actions/get-talent-document-types.md) | GET | Retrieves talent document types from Avionte. |
| [Get Talent Documents](actions/get-talent-documents.md) | GET |  |
| [Get Talent IDs](actions/get-talent-ids.md) | POST |  |
| [Get Talent Onboarding Tasks](actions/get-talent-onboarding-tasks.md) | GET | Retrieves talent onboarding tasks from Avionte. |
| [Get Talent Referrals](actions/get-talent-referrals.md) | GET | Retrieves talent referrals from Avionte. |
| [Get Talent Skills](actions/get-talent-skills.md) | GET | Retrieves talent skills from Avionte. |
| [Get Talent Tags](actions/get-talent-tags.md) | GET |  |
| [Get Web Applicants for a Job](actions/get-web-applicants-for-a-job.md) | GET |  |
| [Get Web Applications for a Talent](actions/get-web-applications-for-a-talent.md) | GET |  |
| [Query Multiple Jobs](actions/query-multiple-jobs.md) | POST |  |
| [Query Multiple Talents](actions/query-multiple-talents.md) | POST |  |
| [Query Multiple Web Applicants](actions/query-multiple-web-applicants.md) | POST |  |
| [Update Talent](actions/update-talent.md) | PUT |  |

