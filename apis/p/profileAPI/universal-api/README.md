# <img src="https://images.mindcloud.co/apps/icons/profile-api_1776802619791.png" alt="profileAPI logo" width="28" height="28"> profileAPI: Universal API

B2B company and person profile enrichment API for finding companies, finding people, and looking up email or phone contact data.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/profileAPI/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 10
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://profileapi.com/
- **Vendor API docs:** https://documentation.profileapi.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Company Find Jobs](actions/list-company-find-jobs.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/profileAPI/latest/actions/list-company-find-jobs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (10)

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Find Companies](actions/find-companies.md) | GET | Finds companies in profileAPI by filter criteria. |

### Company Find Job

| Action | Method | Description |
| --- | --- | --- |
| [Create Company Find Job](actions/create-company-find-job.md) | POST | Creates a company search job in profileAPI. |
| [Get Company Find Job](actions/get-company-find-job.md) | GET | Retrieves a company search job from profileAPI. |
| [Get Latest Company Find Job](actions/get-latest-company-find-job.md) | GET | Retrieves the latest company search job from profileAPI. |
| [List Company Find Jobs](actions/list-company-find-jobs.md) | GET | Retrieves company search jobs from profileAPI. |

### Email Contact

| Action | Method | Description |
| --- | --- | --- |
| [Lookup Email](actions/lookup-email.md) | GET | Finds an email contact in profileAPI by person details. |

### Person

| Action | Method | Description |
| --- | --- | --- |
| [Find Persons](actions/find-persons.md) | GET | Finds persons in profileAPI by filter criteria. |
| [Reverse Lookup Email](actions/reverse-lookup-email.md) | GET | Finds a person in profileAPI by email address. |
| [Reverse Lookup Phone](actions/reverse-lookup-phone.md) | GET | Finds a person in profileAPI by phone number. |

### Phone Contact

| Action | Method | Description |
| --- | --- | --- |
| [Lookup Phone](actions/lookup-phone.md) | GET | Finds a phone contact in profileAPI by person details. |

