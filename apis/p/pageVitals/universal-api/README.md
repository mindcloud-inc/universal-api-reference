# <img src="https://images.mindcloud.co/apps/icons/page-vitals_1774895111462.png" alt="PageVitals logo" width="28" height="28"> PageVitals: Universal API

PageVitals: Monitor websites, tests, budgets, and performance opportunities

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/pageVitals/latest
- **Category:** IT Operations / Observability
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://pagevitals.com
- **Vendor API docs:** https://pagevitals.com/docs/rest-api/reference/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Websites](actions/list-websites.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pageVitals/latest/actions/list-websites?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Budget

| Action | Method | Description |
| --- | --- | --- |
| [Create Budget](actions/create-budget.md) | POST |  |
| [List Budgets](actions/list-budgets.md) | GET |  |
| [Update Budget](actions/update-budget.md) | PUT |  |

### Crux Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Page CrUX Timeline](actions/get-page-crux-timeline.md) | GET |  |

### Field Testing Resource

| Action | Method | Description |
| --- | --- | --- |
| [List Field Testing Resources](actions/list-field-testing-resources.md) | GET |  |

### Multistep Run

| Action | Method | Description |
| --- | --- | --- |
| [List Multistep Test Runs](actions/list-multistep-test-runs.md) | GET |  |
| [Run All Multistep Tests](actions/run-all-multistep-tests.md) | POST |  |
| [Run Multistep Test](actions/run-multistep-test.md) | POST |  |

### Multistep Test

| Action | Method | Description |
| --- | --- | --- |
| [Create Multistep Test](actions/create-multistep-test.md) | POST |  |
| [Get Multistep Test](actions/get-multistep-test.md) | GET |  |
| [List Multistep Tests](actions/list-multistep-tests.md) | GET |  |
| [Update Multistep Test](actions/update-multistep-test.md) | PUT |  |

### Network Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Page Network Chart](actions/get-page-network-chart.md) | GET |  |

### Opportunity

| Action | Method | Description |
| --- | --- | --- |
| [Get Page Opportunity](actions/get-page-opportunity.md) | GET |  |
| [List Page Opportunities](actions/list-page-opportunities.md) | GET |  |
| [List Test Opportunities](actions/list-test-opportunities.md) | GET |  |
| [List Website Opportunities](actions/list-website-opportunities.md) | GET |  |

### Page

| Action | Method | Description |
| --- | --- | --- |
| [Add Settings Pages](actions/add-settings-pages.md) | POST |  |
| [Get Page](actions/get-page.md) | GET |  |
| [List Pages](actions/list-pages.md) | GET |  |
| [List Settings Pages](actions/list-settings-pages.md) | GET |  |
| [Update Settings Page](actions/update-settings-page.md) | PUT |  |

### Page Timeline

| Action | Method | Description |
| --- | --- | --- |
| [Get Page Timeline](actions/get-page-timeline.md) | GET |  |

### Test

| Action | Method | Description |
| --- | --- | --- |
| [Get Test](actions/get-test.md) | GET |  |

### Test Series

| Action | Method | Description |
| --- | --- | --- |
| [List Test Series](actions/list-test-series.md) | GET |  |
| [List Tests in Test Series](actions/list-tests-in-test-series.md) | GET |  |
| [Run Tests](actions/run-tests.md) | POST |  |

### Waterfall

| Action | Method | Description |
| --- | --- | --- |
| [Get Test Waterfall](actions/get-test-waterfall.md) | GET |  |

### Website

| Action | Method | Description |
| --- | --- | --- |
| [Add Website](actions/add-website.md) | POST |  |
| [List Websites](actions/list-websites.md) | GET |  |

