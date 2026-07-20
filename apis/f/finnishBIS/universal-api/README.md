# <img src="https://images.mindcloud.co/apps/icons/favicon-avoindata-prh-fi-48x48_1777483247631.png" alt="Finnish BIS logo" width="28" height="28"> Finnish BIS: Universal API

Public Finnish Business Information System open-data API from the Finnish Patent and Registration Office (PRH) for searching Finnish companies, retrieving code-list descriptions, postal-code data, and the downloadable company register dataset.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/finnishBIS/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 3
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.prh.fi/en/index.html
- **Vendor API docs:** https://avoindata.prh.fi/opendata-ytj-api/v3/schema?lang=en

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Search Companies](actions/search-companies.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/finnishBIS/latest/actions/search-companies?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (3)

### Code List Description

| Action | Method | Description |
| --- | --- | --- |
| [Get Code List Description](actions/get-code-list-description.md) | GET | Retrieves code list details from Finnish BIS. |

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Search Companies](actions/search-companies.md) | GET | Finds companies in Finnish BIS. |

### Post Code

| Action | Method | Description |
| --- | --- | --- |
| [List Post Codes](actions/list-post-codes.md) | GET | Retrieves postal code details from Finnish BIS. |

