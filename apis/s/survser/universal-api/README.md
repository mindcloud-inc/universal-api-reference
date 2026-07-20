# <img src="https://images.mindcloud.co/apps/icons/survser_1775658271794.png" alt="Survser logo" width="28" height="28"> Survser: Universal API

Survser public API wrapper for listing surveys and survey responses via query-string API key authentication.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/survser/latest
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://survser.com
- **Vendor API docs:** https://docs.survser.com/docs/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Surveys](actions/list-surveys.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/survser/latest/actions/list-surveys?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (2)

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [List Survey Responses](actions/list-survey-responses.md) | GET |  |
| [List Surveys](actions/list-surveys.md) | GET |  |

