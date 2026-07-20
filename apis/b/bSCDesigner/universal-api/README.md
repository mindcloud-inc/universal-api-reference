# <img src="https://images.mindcloud.co/apps/icons/bsc-designer-logo-white_1775500012279.png" alt="BSC Designer logo" width="28" height="28"> BSC Designer: Universal API

Cloud-based balanced scorecard and KPI management software for strategy execution, scorecards, indicators, and performance reporting.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/bSCDesigner/latest
- **Category:** Business Intelligence / Analytics & BI
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://bscdesigner.com
- **Vendor API docs:** https://www.webbsc.com/swagger-ui.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Request Count Limit Info](actions/get-request-count-limit-info.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bSCDesigner/latest/actions/get-request-count-limit-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Document

| Action | Method | Description |
| --- | --- | --- |
| [Create Empty Document](actions/create-empty-document.md) | POST |  |
| [Get Document Info](actions/get-document-info.md) | GET |  |
| [List Documents](actions/list-documents.md) | GET |  |

### Document Check Request

| Action | Method | Description |
| --- | --- | --- |
| [Check Document Alerts And WEB SQL Indicators](actions/check-document-alerts-and-websql-indicators.md) | GET |  |

### Document Download

| Action | Method | Description |
| --- | --- | --- |
| [Download Raw Document Content](actions/download-raw-document-content.md) | GET |  |

### Document Map

| Action | Method | Description |
| --- | --- | --- |
| [List Document Maps](actions/list-document-maps.md) | GET |  |

### Document Tree

| Action | Method | Description |
| --- | --- | --- |
| [Get Document Tree](actions/get-document-tree.md) | GET |  |

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [Delete Document](actions/delete-document.md) | DELETE |  |
| [Update Document](actions/update-document.md) | PUT |  |

### Excel Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Excel Report](actions/get-excel-report.md) | GET |  |

### Indicator

| Action | Method | Description |
| --- | --- | --- |
| [Get Indicator Info](actions/get-indicator-info.md) | GET |  |

### Indicator Grouped Value

| Action | Method | Description |
| --- | --- | --- |
| [Get All Indicators Grouped Values](actions/get-all-indicators-grouped-values.md) | GET |  |
| [Get All Indicators Grouped Values By Date Range](actions/get-all-indicators-grouped-values-by-date-range.md) | GET |  |
| [Get Indicator Grouped Values](actions/get-indicator-grouped-values.md) | GET |  |
| [Get Indicator Grouped Values By Date Range](actions/get-indicator-grouped-values-by-date-range.md) | GET |  |

### Indicator Type

| Action | Method | Description |
| --- | --- | --- |
| [Get Indicator Types](actions/get-indicator-types.md) | GET |  |

### Indicator Value

| Action | Method | Description |
| --- | --- | --- |
| [Get All Indicator Values For Document](actions/get-all-indicator-values-for-document.md) | GET |  |
| [Get Indicator Value](actions/get-indicator-value.md) | GET |  |
| [Get Selected Indicator Values](actions/get-selected-indicator-values.md) | GET |  |

### Indicator Values

| Action | Method | Description |
| --- | --- | --- |
| [Get Indicator Values At Date](actions/get-indicator-values-at-date.md) | GET |  |

### Initiative Status

| Action | Method | Description |
| --- | --- | --- |
| [List Initiative Statuses](actions/list-initiative-statuses.md) | GET |  |

### Kpi

| Action | Method | Description |
| --- | --- | --- |
| [List KPIs](actions/list-kpis.md) | GET |  |

### Kpi Tree

| Action | Method | Description |
| --- | --- | --- |
| [List KPI Tree](actions/list-kpi-tree.md) | GET |  |

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [Get Organization Info](actions/get-organization-info.md) | GET |  |

### Scorecards

| Action | Method | Description |
| --- | --- | --- |
| [Balance Scorecard](actions/balance-scorecard.md) | PUT |  |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Create Indicator Initiative](actions/create-indicator-initiative.md) | POST |  |
| [Delete Indicator Baseline At Date](actions/delete-indicator-baseline-at-date.md) | DELETE |  |
| [Delete Indicator Initiative](actions/delete-indicator-initiative.md) | DELETE |  |
| [Delete Indicator Max At Date](actions/delete-indicator-max-at-date.md) | DELETE |  |
| [Delete Indicator Min At Date](actions/delete-indicator-min-at-date.md) | DELETE |  |
| [Delete Indicator Score At Date](actions/delete-indicator-score-at-date.md) | DELETE |  |
| [Delete Indicator Target At Date](actions/delete-indicator-target-at-date.md) | DELETE |  |
| [Delete Indicator Values At Date](actions/delete-indicator-values-at-date.md) | DELETE |  |
| [Get Indicator Initiative](actions/get-indicator-initiative.md) | GET |  |
| [Get Request Count Limit Info](actions/get-request-count-limit-info.md) | GET |  |
| [List Indicator Initiatives](actions/list-indicator-initiatives.md) | GET |  |
| [Set Indicator Info](actions/set-indicator-info.md) | PUT |  |
| [Set Indicator Values](actions/set-indicator-values.md) | PUT |  |
| [Set Selected Indicator Values](actions/set-selected-indicator-values.md) | PUT |  |
| [Update Indicator Initiative](actions/update-indicator-initiative.md) | PUT |  |

