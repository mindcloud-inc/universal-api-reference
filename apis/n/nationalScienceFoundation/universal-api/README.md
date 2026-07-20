# <img src="https://images.mindcloud.co/apps/icons/national-science-foundation_1776439958284.png" alt="National Science Foundation logo" width="28" height="28"> National Science Foundation: Universal API

Search and retrieve public NSF award records, funding metadata, and project outcomes.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/nationalScienceFoundation/latest
- **Category:** Content & Files / Storage
- **Actions:** 3
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.nsf.gov
- **Vendor API docs:** https://resources.research.gov/common/webapi/awardapisearch-v1.htm

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Search Awards](actions/search-awards.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nationalScienceFoundation/latest/actions/search-awards?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (3)

### Award

| Action | Method | Description |
| --- | --- | --- |
| [Get Award](actions/get-award.md) | GET | Retrieves award information from National Science Foundation by ID. |
| [Search Awards](actions/search-awards.md) | GET | Finds awards in National Science Foundation by search criteria. |

### Project Outcome Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Award Project Outcomes](actions/get-award-project-outcomes.md) | GET | Retrieves a project outcomes report from National Science Foundation. |

