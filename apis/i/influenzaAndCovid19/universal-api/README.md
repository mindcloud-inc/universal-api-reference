# <img src="https://images.mindcloud.co/apps/icons/influenza-and-covid19_1777392947854.png" alt="Influenza and Covid-19 logo" width="28" height="28"> Influenza and Covid-19: Universal API

Access public CDC respiratory surveillance datasets for influenza, COVID-19, RSV, and combined respiratory illness metrics from Data.CDC.gov.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/influenzaAndCovid19/latest
- **Actions:** 4
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://data.cdc.gov
- **Vendor API docs:** https://dev.socrata.com/docs/endpoints.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Emergency Department Visits by Demographic Category](actions/list-emergency-department-visits-by-demographic-category.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/influenzaAndCovid19/latest/actions/list-emergency-department-visits-by-demographic-category?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (4)

### Emergency Department Respiratory Daily

| Action | Method | Description |
| --- | --- | --- |
| [List Emergency Department Respiratory Daily](actions/list-emergency-department-respiratory-daily.md) | GET |  |

### Emergency Department Visits By Demographic Category

| Action | Method | Description |
| --- | --- | --- |
| [List Emergency Department Visits by Demographic Category](actions/list-emergency-department-visits-by-demographic-category.md) | GET |  |

### Provisional Respiratory Death Percentages

| Action | Method | Description |
| --- | --- | --- |
| [List Provisional Respiratory Death Percentages](actions/list-provisional-respiratory-death-percentages.md) | GET |  |

### Viral Respiratory Test Positivity

| Action | Method | Description |
| --- | --- | --- |
| [List Viral Respiratory Test Positivity](actions/list-viral-respiratory-test-positivity.md) | GET |  |

