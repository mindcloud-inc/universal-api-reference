# <img src="https://images.mindcloud.co/apps/icons/33babbf4-122d-4aab-86d2-bc31933de3cc-0_1776706058616.png" alt="Grants.gov logo" width="28" height="28"> Grants.gov: Universal API

Search public federal grant opportunities and retrieve opportunity details through the Grants.gov Applicant REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/grantsgov/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.grants.gov
- **Vendor API docs:** https://grants.gov/api/api-guide

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Fetch Opportunity](actions/fetch-opportunity.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/grantsgov/latest/actions/fetch-opportunity?connectionId=$CONNECTION_ID&opportunityId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (2)

### Opportunities

| Action | Method | Description |
| --- | --- | --- |
| [Fetch Opportunity](actions/fetch-opportunity.md) | GET | Retrieves grant opportunity details from Grants.gov by opportunity ID. |
| [Search Opportunities](actions/search-opportunities.md) | GET | Finds grant opportunities in Grants.gov by public search filters. |

