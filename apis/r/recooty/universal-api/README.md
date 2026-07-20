# <img src="https://images.mindcloud.co/apps/icons/recooty-icon_1775833945850.png" alt="Recooty logo" width="28" height="28"> Recooty: Universal API

Access Recooty public job listings with an API key and candidate endpoints with a personal access token.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/recooty/latest
- **Actions:** 5
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://recooty.com/
- **Vendor API docs:** https://api.recooty.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Jobs](actions/list-jobs.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/recooty/latest/actions/list-jobs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (5)

### Application

| Action | Method | Description |
| --- | --- | --- |
| [Create Application](actions/create-application.md) | POST |  |
| [Get Application](actions/get-application.md) | GET |  |
| [List Applications](actions/list-applications.md) | GET |  |

### Job

| Action | Method | Description |
| --- | --- | --- |
| [Get Job](actions/get-job.md) | GET |  |
| [List Jobs](actions/list-jobs.md) | GET |  |

