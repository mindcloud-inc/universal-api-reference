# <img src="https://images.mindcloud.co/apps/icons/company-urlfinder_1774903914875.png" alt="Company URL Finder logo" width="28" height="28"> Company URL Finder: Universal API

Convert company names into verified website domains and domains into company names using Company URL Finder's company enrichment API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/companyURLFinder/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 3
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://companyurlfinder.com/
- **Vendor API docs:** https://apidocs.companyurlfinder.com/apis

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Company Query to LinkedIn URL](actions/company-query-to-linkedin-url.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/companyURLFinder/latest/actions/company-query-to-linkedin-url?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (3)

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [Company Query to LinkedIn URL](actions/company-query-to-linkedin-url.md) | GET | Finds a company's LinkedIn URL in Company URL Finder. |
| [Get Company Name by Domain](actions/get-company-name-by-domain.md) | GET | Finds a company name in Company URL Finder by domain. |
| [Get Domain by Company Name](actions/get-domain-by-company-name.md) | GET | Finds a company's domain in Company URL Finder by company name. |

