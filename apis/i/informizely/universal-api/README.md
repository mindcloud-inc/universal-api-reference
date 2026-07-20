# <img src="https://images.mindcloud.co/apps/icons/informizely-icon_1775578870525.jpeg" alt="Informizely logo" width="28" height="28"> Informizely: Universal API

Informizely is a customer feedback and survey platform with a REST Reporting API for retrieving site, survey, response, question, count, and statistics data.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/informizely/latest
- **Category:** Productivity / Forms & Surveys
- **Actions:** 7
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.informizely.com/
- **Vendor API docs:** https://www.informizely.com/help/report-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Sites](actions/list-sites.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/informizely/latest/actions/list-sites?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (7)

### Question

| Action | Method | Description |
| --- | --- | --- |
| [List Questions](actions/list-questions.md) | GET |  |

### Response

| Action | Method | Description |
| --- | --- | --- |
| [Get Response Count](actions/get-response-count.md) | GET |  |
| [List Responses](actions/list-responses.md) | GET |  |

### Site

| Action | Method | Description |
| --- | --- | --- |
| [List Sites](actions/list-sites.md) | GET |  |

### Survey

| Action | Method | Description |
| --- | --- | --- |
| [Get All Survey Data](actions/get-all-survey-data.md) | GET |  |
| [Get Survey Stats](actions/get-survey-stats.md) | GET |  |
| [List Surveys](actions/list-surveys.md) | GET |  |

