# BSC Designer: Native API Reference

A consolidated summary of BSC Designer's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://www.webbsc.com/swagger-ui.html
- **OpenAPI specification:** https://www.webbsc.com/v2/api-docs
- **API base URL:** `https://www.webbsc.com`

## Authentication

### API Token

Paste a BSC Designer API token obtained from POST /rest/login using the account owner's email and password. The app sends this value in the required token header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
token: <apiKey>
```

[Official authentication documentation](https://bscdesigner.com/webbsc_manual/bsc_designer_online.pdf)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Balance Scorecard](actions/balance-scorecard.md) | `PUT /rest/api/document/:docId/kpi/weight-balance` | [docs](https://www.webbsc.com/swagger-ui.html#/rest-document-controller/runStrategyMapWizardUsingPUT) |
| [Check Document Alerts And WEB SQL Indicators](actions/check-document-alerts-and-websql-indicators.md) | `POST /rest/api/document/:docId/document-check-requests` | [docs](https://www.webbsc.com/swagger-ui.html#/rest-document-controller/checkDocumentUsingPOST) |
| [Create Empty Document](actions/create-empty-document.md) | `POST /rest/api/documents` | [docs](https://www.webbsc.com/swagger-ui.html#/rest-document-list-controller/createDocumentUsingPOST) |
| [Create Indicator Initiative](actions/create-indicator-initiative.md) | `POST /rest/api/document/:docId/kpi/:guid/initiatives` | [docs](https://www.webbsc.com/swagger-ui.html#/rest-kpi-initiative-controller/createInitiativeUsingPOST) |
| [Delete Document](actions/delete-document.md) | `DELETE /rest/api/documents/list/:id` | [docs](https://www.webbsc.com/swagger-ui.html#/rest-document-list-controller/deleteDocumentUsingDELETE) |
| [Delete Indicator Baseline At Date](actions/delete-indicator-baseline-at-date.md) | `DELETE /rest/api/document/:documentId/kpi/indicator/:indicatorGuid/baseline/:date` | [docs](https://www.webbsc.com/swagger-ui.html#/rest-kpi-value-controller/deleteBaselineAtUsingDELETE) |
| [Delete Indicator Initiative](actions/delete-indicator-initiative.md) | `DELETE /rest/api/document/:docId/kpi/:guid/initiatives/:initiativeGuid` | [docs](https://www.webbsc.com/swagger-ui.html#/rest-kpi-initiative-controller/removeInitiativeUsingDELETE) |
| [Delete Indicator Max At Date](actions/delete-indicator-max-at-date.md) | `DELETE /rest/api/document/:documentId/kpi/indicator/:indicatorGuid/max/:date` | [docs](https://www.webbsc.com/swagger-ui.html#/rest-kpi-value-controller/deleteMaxAtUsingDELETE) |
| [Delete Indicator Min At Date](actions/delete-indicator-min-at-date.md) | `DELETE /rest/api/document/:documentId/kpi/indicator/:indicatorGuid/min/:date` | [docs](https://www.webbsc.com/swagger-ui.html#/rest-kpi-value-controller/deleteMinAtUsingDELETE) |
| [Delete Indicator Score At Date](actions/delete-indicator-score-at-date.md) | `DELETE /rest/api/document/:documentId/kpi/indicator/:indicatorGuid/score/:date` | [docs](https://www.webbsc.com/swagger-ui.html#/rest-kpi-value-controller/deleteScoreAtUsingDELETE) |
| [Delete Indicator Target At Date](actions/delete-indicator-target-at-date.md) | `DELETE /rest/api/document/:documentId/kpi/indicator/:indicatorGuid/target/:date` | [docs](https://www.webbsc.com/swagger-ui.html#/rest-kpi-value-controller/deleteTargetAtUsingDELETE) |
| [Delete Indicator Values At Date](actions/delete-indicator-values-at-date.md) | `DELETE /rest/api/document/:documentId/kpi/indicator/:indicatorGuid/values/:date` | [docs](https://www.webbsc.com/swagger-ui.html#/rest-kpi-value-controller/deleteValueAtUsingDELETE) |
| [Download Raw Document Content](actions/download-raw-document-content.md) | `GET /rest/api/document/:docId/download` | [docs](https://www.webbsc.com/swagger-ui.html#/rest-document-controller/downloadDocumentUsingGET) |
| [Get All Indicator Values For Document](actions/get-all-indicator-values-for-document.md) | `GET /rest/api/document/:docId/kpi/batch/all/get-value/:date` | [docs](https://www.webbsc.com/swagger-ui.html#/rest-kpi-value-controller/getAllValuesUsingGET) |
| [Get All Indicators Grouped Values](actions/get-all-indicators-grouped-values.md) | `GET /rest/api/document/:docId/kpi/indicatos/grouped-value/:period` | [docs](https://www.webbsc.com/swagger-ui.html#/rest-kpi-grouped-values-controller/getBatchByPeriodUsingGET) |
| [Get All Indicators Grouped Values By Date Range](actions/get-all-indicators-grouped-values-by-date-range.md) | `GET /rest/api/document/:docId/kpi/indicators/grouped-value/:period/:startDate/:endDate` | [docs](https://www.webbsc.com/swagger-ui.html#/rest-kpi-grouped-values-controller/getBatchByPeriodAndDatesUsingGET) |
| [Get Document Info](actions/get-document-info.md) | `GET /rest/api/documents/list/:idOrAlias` | [docs](https://www.webbsc.com/swagger-ui.html#/rest-document-list-controller/getDocumentInfoUsingGET) |
| [Get Document Tree](actions/get-document-tree.md) | `GET /rest/api/documents/tree` | [docs](https://www.webbsc.com/swagger-ui.html#/rest-document-list-controller/getDocumentTreeUsingGET) |
| [Get Excel Report](actions/get-excel-report.md) | `GET /rest/api/report/:id/excel` | [docs](https://www.webbsc.com/swagger-ui.html#/report-controller/getExcelReportAtDateForRestUsingGET) |
| [Get Indicator Grouped Values](actions/get-indicator-grouped-values.md) | `GET /rest/api/document/:docId/kpi/indicator/:guid/grouped-value/:period` | [docs](https://www.webbsc.com/swagger-ui.html#/rest-kpi-grouped-values-controller/getByPeriodUsingGET) |
| [Get Indicator Grouped Values By Date Range](actions/get-indicator-grouped-values-by-date-range.md) | `GET /rest/api/document/:docId/kpi/indicator/:guid/grouped-value/:period/:startDate/:endDate` | [docs](https://www.webbsc.com/swagger-ui.html#/rest-kpi-grouped-values-controller/getByPeriodAndDatesUsingGET) |
| [Get Indicator Info](actions/get-indicator-info.md) | `GET /rest/api/document/:docId/kpi/:guid` | [docs](https://www.webbsc.com/swagger-ui.html#/rest-kpi-controller/getKpiUsingGET) |
| [Get Indicator Initiative](actions/get-indicator-initiative.md) | `GET /rest/api/document/:docId/kpi/:guid/initiatives/:initiativeGuid` | [docs](https://www.webbsc.com/swagger-ui.html#/rest-kpi-initiative-controller/getInitiativeUsingGET) |
| [Get Indicator Types](actions/get-indicator-types.md) | `GET /rest/api/service/enums/indicator-types` | [docs](https://www.webbsc.com/swagger-ui.html#/rest-kpi-controller/getIndicatorBusinessTypeUsingGET) |
| [Get Indicator Value](actions/get-indicator-value.md) | `GET /rest/api/document/:docId/kpi/indicator/:guid/value/:date` | [docs](https://www.webbsc.com/swagger-ui.html#/rest-kpi-value-controller/getSingleValueUsingGET) |
| [Get Indicator Values At Date](actions/get-indicator-values-at-date.md) | `GET /rest/api/document/:documentId/kpi/indicator/:indicatorGuid/values/:date` | [docs](https://www.webbsc.com/swagger-ui.html#/rest-kpi-value-controller/getValueAtUsingGET) |
| [Get Organization Info](actions/get-organization-info.md) | `GET /rest/api/organization-info` | [docs](https://www.webbsc.com/swagger-ui.html#/organization-info-rest-controller/getOrganizationInfoModelUsingGET) |
| [Get Request Count Limit Info](actions/get-request-count-limit-info.md) | `GET /rest/api/access/info` | [docs](https://www.webbsc.com/swagger-ui.html#/access-limit-rest-controller/getInfoUsingGET) |
| [Get Selected Indicator Values](actions/get-selected-indicator-values.md) | `POST /rest/api/document/:docId/kpi/batch/get-value/:date` | [docs](https://www.webbsc.com/swagger-ui.html#/rest-kpi-value-controller/getChosenValuesUsingPOST) |
| [List Document Maps](actions/list-document-maps.md) | `GET /rest/api/document/:docId/maps` | [docs](https://www.webbsc.com/swagger-ui.html#/rest-document-map-controller/getMapsUsingGET) |
| [List Documents](actions/list-documents.md) | `GET /rest/api/documents/list` | [docs](https://www.webbsc.com/swagger-ui.html#/rest-document-list-controller/getDocumentsListUsingGET) |
| [List Indicator Initiatives](actions/list-indicator-initiatives.md) | `GET /rest/api/document/:docId/kpi/:guid/initiatives` | [docs](https://www.webbsc.com/swagger-ui.html#/rest-kpi-initiative-controller/getInitiativesUsingGET) |
| [List Initiative Statuses](actions/list-initiative-statuses.md) | `GET /rest/api/initiative-statuses` | [docs](https://www.webbsc.com/swagger-ui.html#/rest-kpi-initiative-controller/getAllAvailableInitiativeStatusesUsingGET) |
| [List KPI Tree](actions/list-kpi-tree.md) | `GET /rest/api/document/:docId/kpi/tree` | [docs](https://www.webbsc.com/swagger-ui.html#/rest-document-controller/getKpiTreeUsingGET) |
| [List KPIs](actions/list-kpis.md) | `GET /rest/api/document/:docId/kpi/list` | [docs](https://www.webbsc.com/swagger-ui.html#/rest-document-controller/getKpiListUsingGET) |
| [Set Indicator Info](actions/set-indicator-info.md) | `PUT /rest/api/document/:docId/kpi/:guid` | [docs](https://www.webbsc.com/swagger-ui.html#/rest-kpi-controller/setKpiUsingPUT) |
| [Set Indicator Values](actions/set-indicator-values.md) | `POST /rest/api/document/:docId/kpi/indicator/:guid/value/:date` | [docs](https://www.webbsc.com/swagger-ui.html#/rest-kpi-value-controller/setSingleValueUsingPOST) |
| [Set Selected Indicator Values](actions/set-selected-indicator-values.md) | `POST /rest/api/document/:docId/kpi/batch/set-value/:date` | [docs](https://www.webbsc.com/swagger-ui.html#/rest-kpi-value-controller/setChosenValuesUsingPOST) |
| [Update Document](actions/update-document.md) | `PUT /rest/api/documents/list/:id` | [docs](https://www.webbsc.com/swagger-ui.html#/rest-document-list-controller/updateDocumentUsingPUT) |
| [Update Indicator Initiative](actions/update-indicator-initiative.md) | `PUT /rest/api/document/:docId/kpi/:guid/initiatives/:initiativeGuid` | [docs](https://www.webbsc.com/swagger-ui.html#/rest-kpi-initiative-controller/updateInitiativeUsingPUT) |
