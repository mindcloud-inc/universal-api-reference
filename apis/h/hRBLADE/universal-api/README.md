# <img src="https://images.mindcloud.co/apps/icons/hrblade-icon-filled-256_1775239523872.png" alt="HRBLADE logo" width="28" height="28"> HRBLADE: Universal API

HRBLADE hiring platform API for jobs, candidates, responses, users, and company administration.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/hRBLADE/latest
- **Category:** Human Resources / Recruiting
- **Actions:** 19
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://hrblade.com
- **Vendor API docs:** https://hrblade.com/docs/developers/api-reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get User](actions/get-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hRBLADE/latest/actions/get-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (19)

### Candidates

| Action | Method | Description |
| --- | --- | --- |
| [Invite Candidates By Email](actions/invite-candidates-by-email.md) | POST |  |

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [Create Company](actions/create-company.md) | POST |  |
| [Get Company](actions/get-company.md) | GET |  |
| [List Companies](actions/list-companies.md) | GET |  |
| [Update Company](actions/update-company.md) | PUT |  |

### Config

| Action | Method | Description |
| --- | --- | --- |
| [Get Config](actions/get-config.md) | GET |  |

### Jobs

| Action | Method | Description |
| --- | --- | --- |
| [Create Job](actions/create-job.md) | POST |  |
| [Get Job](actions/get-job.md) | GET |  |
| [List Jobs](actions/list-jobs.md) | GET |  |
| [Remove Job](actions/remove-job.md) | DELETE |  |
| [Update Job](actions/update-job.md) | PUT |  |
| [Update Job Status](actions/update-job-status.md) | PUT |  |

### Response

| Action | Method | Description |
| --- | --- | --- |
| [Get Response](actions/get-response.md) | GET |  |
| [Update Response Rating](actions/update-response-rating.md) | PUT |  |
| [Update Response Status](actions/update-response-status.md) | PUT |  |

### Sessions

| Action | Method | Description |
| --- | --- | --- |
| [Login](actions/login.md) | POST |  |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get User](actions/get-user.md) | GET |  |
| [List Users](actions/list-users.md) | GET |  |
| [Update User Settings](actions/update-user-settings.md) | PUT |  |

