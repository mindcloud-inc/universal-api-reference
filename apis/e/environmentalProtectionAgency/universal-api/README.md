# <img src="https://images.mindcloud.co/apps/icons/seal-of-the-united-states-environmental-protection-agency_1776801662926.png" alt="Environmental Protection Agency logo" width="28" height="28"> Environmental Protection Agency: Universal API

Access EPA Air Quality System (AQS) metadata, monitor inventory, ambient air sample measurements, summary data, and quality assurance records.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/environmentalProtectionAgency/latest
- **Category:** Business Intelligence / Analytics & BI
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.epa.gov
- **Vendor API docs:** https://aqs.epa.gov/aqsweb/documents/data_api.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List States](actions/list-states.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/environmentalProtectionAgency/latest/actions/list-states?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Annual Summary

| Action | Method | Description |
| --- | --- | --- |
| [Get Annual Data By Box](actions/get-annual-data-by-box.md) | GET | Retrieves annual summary data for a bounding box from EPA AQS. |
| [Get Annual Data By CBSA](actions/get-annual-data-by-cbsa.md) | GET | Retrieves annual summary data for a CBSA from EPA AQS. |
| [Get Annual Data By County](actions/get-annual-data-by-county.md) | GET | Retrieves annual summary data for a county from EPA AQS. |
| [Get Annual Data By Site](actions/get-annual-data-by-site.md) | GET | Retrieves annual summary data for a site from EPA AQS. |
| [Get Annual Data By State](actions/get-annual-data-by-state.md) | GET | Retrieves annual summary data for a state from EPA AQS. |

### Api Availability

| Action | Method | Description |
| --- | --- | --- |
| [Check API Availability](actions/check-api-availability.md) | GET | Retrieves API availability status from EPA AQS. |

### Cbsa

| Action | Method | Description |
| --- | --- | --- |
| [List CBSAs](actions/list-cbsas.md) | GET | Retrieves CBSAs from EPA AQS. |

### County

| Action | Method | Description |
| --- | --- | --- |
| [List Counties By State](actions/list-counties-by-state.md) | GET | Retrieves counties for a state from EPA AQS. |

### Daily Summary

| Action | Method | Description |
| --- | --- | --- |
| [Get Daily Data By Box](actions/get-daily-data-by-box.md) | GET | Retrieves daily summary data for a bounding box from EPA AQS. |
| [Get Daily Data By CBSA](actions/get-daily-data-by-cbsa.md) | GET | Retrieves daily summary data for a CBSA from EPA AQS. |
| [Get Daily Data By County](actions/get-daily-data-by-county.md) | GET | Retrieves daily summary data for a county from EPA AQS. |
| [Get Daily Data By Site](actions/get-daily-data-by-site.md) | GET | Retrieves daily summary data for a site from EPA AQS. |
| [Get Daily Data By State](actions/get-daily-data-by-state.md) | GET | Retrieves daily summary data for a state from EPA AQS. |

### Known Issue

| Action | Method | Description |
| --- | --- | --- |
| [List Known Issues](actions/list-known-issues.md) | GET | Retrieves known issues from EPA AQS. |

### Monitor

| Action | Method | Description |
| --- | --- | --- |
| [Get Monitors By Box](actions/get-monitors-by-box.md) | GET | Retrieves monitors for a bounding box from EPA AQS. |
| [Get Monitors By CBSA](actions/get-monitors-by-cbsa.md) | GET | Retrieves monitors for a CBSA from EPA AQS. |
| [Get Monitors By County](actions/get-monitors-by-county.md) | GET | Retrieves monitors for a county from EPA AQS. |
| [Get Monitors By Site](actions/get-monitors-by-site.md) | GET | Retrieves monitors for a site from EPA AQS. |
| [Get Monitors By State](actions/get-monitors-by-state.md) | GET | Retrieves monitors for a state from EPA AQS. |

### Monitoring Agency

| Action | Method | Description |
| --- | --- | --- |
| [List Monitoring Agencies](actions/list-monitoring-agencies.md) | GET | Retrieves monitoring agencies from EPA AQS. |

### Monitoring Site

| Action | Method | Description |
| --- | --- | --- |
| [List Sites By County](actions/list-sites-by-county.md) | GET | Retrieves monitoring sites for a county from EPA AQS. |

### Parameter

| Action | Method | Description |
| --- | --- | --- |
| [List Parameters By Class](actions/list-parameters-by-class.md) | GET | Retrieves parameters for a class from EPA AQS. |

### Parameter Class

| Action | Method | Description |
| --- | --- | --- |
| [List Parameter Classes](actions/list-parameter-classes.md) | GET | Retrieves parameter classes from EPA AQS. |

### Primary Quality Assurance Organization

| Action | Method | Description |
| --- | --- | --- |
| [List PQAOs](actions/list-pqaos.md) | GET | Retrieves primary quality assurance organizations from EPA AQS. |

### Qa Annual Performance Evaluation

| Action | Method | Description |
| --- | --- | --- |
| [Get QA Annual Performance Evaluations By County](actions/get-qa-annual-performance-evaluations-by-county.md) | GET | Retrieves QA annual performance evaluations for a county from EPA AQS. |
| [Get QA Annual Performance Evaluations By Site](actions/get-qa-annual-performance-evaluations-by-site.md) | GET | Retrieves QA annual performance evaluations for a site from EPA AQS. |
| [Get QA Annual Performance Evaluations By State](actions/get-qa-annual-performance-evaluations-by-state.md) | GET | Retrieves QA annual performance evaluations for a state from EPA AQS. |

### Quarterly Summary

| Action | Method | Description |
| --- | --- | --- |
| [Get Quarterly Data By Box](actions/get-quarterly-data-by-box.md) | GET | Retrieves quarterly summary data for a bounding box from EPA AQS. |
| [Get Quarterly Data By CBSA](actions/get-quarterly-data-by-cbsa.md) | GET | Retrieves quarterly summary data for a CBSA from EPA AQS. |
| [Get Quarterly Data By County](actions/get-quarterly-data-by-county.md) | GET | Retrieves quarterly summary data for a county from EPA AQS. |
| [Get Quarterly Data By Site](actions/get-quarterly-data-by-site.md) | GET | Retrieves quarterly summary data for a site from EPA AQS. |
| [Get Quarterly Data By State](actions/get-quarterly-data-by-state.md) | GET | Retrieves quarterly summary data for a state from EPA AQS. |

### Revision History

| Action | Method | Description |
| --- | --- | --- |
| [List Revision History](actions/list-revision-history.md) | GET | Retrieves revision history from EPA AQS. |

### Sample Data

| Action | Method | Description |
| --- | --- | --- |
| [Get Sample Data By Box](actions/get-sample-data-by-box.md) | GET | Retrieves sample data for a bounding box from EPA AQS. |
| [Get Sample Data By CBSA](actions/get-sample-data-by-cbsa.md) | GET | Retrieves sample data for a CBSA from EPA AQS. |
| [Get Sample Data By County](actions/get-sample-data-by-county.md) | GET | Retrieves sample data for a county from EPA AQS. |
| [Get Sample Data By Site](actions/get-sample-data-by-site.md) | GET | Retrieves sample data for a site from EPA AQS. |
| [Get Sample Data By State](actions/get-sample-data-by-state.md) | GET | Retrieves sample data for a state from EPA AQS. |

### Service Field

| Action | Method | Description |
| --- | --- | --- |
| [List Fields By Service](actions/list-fields-by-service.md) | GET | Retrieves field definitions for a selected EPA AQS service. |

### State

| Action | Method | Description |
| --- | --- | --- |
| [List States](actions/list-states.md) | GET | Retrieves states from EPA AQS. |

