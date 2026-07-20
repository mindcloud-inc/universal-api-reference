# <img src="https://images.mindcloud.co/apps/icons/remote-ok_1777046264340.png" alt="Remote OK logo" width="28" height="28"> Remote OK: Universal API

Remote OK: List public remote job postings

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/remoteOK/latest
- **Category:** Human Resources / Recruiting
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://remoteok.com
- **Vendor API docs:** https://remoteok.com/json

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Remote Jobs](actions/list-remote-jobs.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/remoteOK/latest/actions/list-remote-jobs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Remote Job

| Action | Method | Description |
| --- | --- | --- |
| [List Remote Jobs](actions/list-remote-jobs.md) | GET | Retrieves remote job postings from Remote OK. |

