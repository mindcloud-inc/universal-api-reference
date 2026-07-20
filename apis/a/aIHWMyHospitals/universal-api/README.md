# <img src="https://images.mindcloud.co/apps/icons/aihw-icon_1777557962365.png" alt="AIHW MyHospitals logo" width="28" height="28"> AIHW MyHospitals: Universal API

Access current Australian hospital data from the Australian Institute of Health and Welfare MyHospitals Data API, including measures, reported measures, datasets, reporting units, and flat data extracts.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/aIHWMyHospitals/latest
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.aihw.gov.au/reports-data/myhospitals
- **Vendor API docs:** https://www.aihw.gov.au/reports-data/myhospitals/content/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Dataset](actions/get-dataset.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aIHWMyHospitals/latest/actions/get-dataset?connectionId=$CONNECTION_ID&datasetId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Brick Availability

| Action | Method | Description |
| --- | --- | --- |
| [List Bricks Available For Reporting Unit](actions/list-bricks-available-for-reporting-unit.md) | GET | Retrieves available brick codes for a reporting unit in AIHW MyHospitals. |
| [List Bricks Available For Reporting Unit Type](actions/list-bricks-available-for-reporting-unit-type.md) | GET | Retrieves available bricks by reporting unit for a type in AIHW MyHospitals. |

### Data Item

| Action | Method | Description |
| --- | --- | --- |
| [List Data Items For Dataset](actions/list-data-items-for-dataset.md) | GET | Retrieves data items for a dataset from AIHW MyHospitals. |
| [List Data Items For Measure](actions/list-data-items-for-measure.md) | GET | Retrieves data items for a measure from AIHW MyHospitals. |
| [List Data Items For Reported Measure](actions/list-data-items-for-reported-measure.md) | GET | Retrieves data items for a reported measure from AIHW MyHospitals. |
| [List Data Items For Reporting Unit](actions/list-data-items-for-reporting-unit.md) | GET | Retrieves data items for a reporting unit from AIHW MyHospitals. |

### Dataset

| Action | Method | Description |
| --- | --- | --- |
| [Get Dataset](actions/get-dataset.md) | GET | Retrieves a dataset from AIHW MyHospitals. |
| [List Datasets](actions/list-datasets.md) | GET | Retrieves available datasets from AIHW MyHospitals. |

### Flat Data Extract

| Action | Method | Description |
| --- | --- | --- |
| [List Flat Data Extract](actions/list-flat-data-extract.md) | GET | Retrieves flat data for a measure category from AIHW MyHospitals. |

### Flat Formatted Data Extract

| Action | Method | Description |
| --- | --- | --- |
| [List Flat Formatted Data Extract](actions/list-flat-formatted-data-extract.md) | GET | Retrieves flat formatted data for a measure category from AIHW MyHospitals. |

### Measure

| Action | Method | Description |
| --- | --- | --- |
| [Get Measure](actions/get-measure.md) | GET | Retrieves a measure from AIHW MyHospitals. |
| [List Measures](actions/list-measures.md) | GET | Retrieves all measures from AIHW MyHospitals. |
| [List Measures Available For Reporting Unit](actions/list-measures-available-for-reporting-unit.md) | GET | Retrieves measures with data for a reporting unit in AIHW MyHospitals. |
| [List Measures For Measure Category](actions/list-measures-for-measure-category.md) | GET | Retrieves measures for a measure category from AIHW MyHospitals. |

### Measure Category

| Action | Method | Description |
| --- | --- | --- |
| [List Measure Categories](actions/list-measure-categories.md) | GET | Retrieves measure categories from AIHW MyHospitals. |

### Reported Measure

| Action | Method | Description |
| --- | --- | --- |
| [Get Reported Measure](actions/get-reported-measure.md) | GET | Retrieves a reported measure from AIHW MyHospitals. |
| [List Reported Measures](actions/list-reported-measures.md) | GET | Retrieves all reported measures from AIHW MyHospitals. |
| [List Reported Measures For Category](actions/list-reported-measures-for-category.md) | GET | Retrieves reported measures for a category from AIHW MyHospitals. |

### Reported Measure Category

| Action | Method | Description |
| --- | --- | --- |
| [Get Reported Measure Category](actions/get-reported-measure-category.md) | GET | Retrieves a reported measure category from AIHW MyHospitals. |
| [List Reported Measure Categories](actions/list-reported-measure-categories.md) | GET | Retrieves reported measure categories from AIHW MyHospitals. |

### Reporting Unit

| Action | Method | Description |
| --- | --- | --- |
| [Get Reporting Unit](actions/get-reporting-unit.md) | GET | Retrieves a reporting unit from AIHW MyHospitals. |
| [List Reporting Units](actions/list-reporting-units.md) | GET | Retrieves reporting units from AIHW MyHospitals. |
| [List Reporting Units Available For Measure](actions/list-reporting-units-available-for-measure.md) | GET | Retrieves reporting units with data for a measure in AIHW MyHospitals. |

### Reporting Unit Type

| Action | Method | Description |
| --- | --- | --- |
| [List Reporting Unit Types](actions/list-reporting-unit-types.md) | GET | Retrieves reporting unit types from AIHW MyHospitals. |

