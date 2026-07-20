# <img src="https://images.mindcloud.co/apps/icons/bea-final-logo-blue-backing_1778000497400.png" alt="Bureau of Economic Analysis logo" width="28" height="28"> Bureau of Economic Analysis: Universal API

Access BEA published economic statistics and metadata, including national, regional, international, and industry account datasets.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/bureauOfEconomicAnalysis/latest
- **Category:** Business Intelligence / Analytics & BI
- **Actions:** 17
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.bea.gov
- **Vendor API docs:** https://apps.bea.gov/api/_pdf/bea_web_service_api_user_guide.pdf

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Dataset List](actions/get-dataset-list.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bureauOfEconomicAnalysis/latest/actions/get-dataset-list?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (17)

### Api Dataset Metadata

| Action | Method | Description |
| --- | --- | --- |
| [Get API Dataset Metadata](actions/get-api-dataset-metadata.md) | GET | Retrieves API dataset metadata from the Bureau of Economic Analysis. |

### Dataset

| Action | Method | Description |
| --- | --- | --- |
| [Get Dataset List](actions/get-dataset-list.md) | GET | Retrieves available datasets from the Bureau of Economic Analysis. |

### Filtered Parameter Value

| Action | Method | Description |
| --- | --- | --- |
| [Get Filtered Parameter Values](actions/get-filtered-parameter-values.md) | GET | Retrieves filtered parameter values for a Bureau of Economic Analysis dataset. |

### Fixed Assets Data

| Action | Method | Description |
| --- | --- | --- |
| [Get Fixed Assets Data](actions/get-fixed-assets-data.md) | GET | Retrieves fixed assets data from the Bureau of Economic Analysis. |

### Gdp By Industry Data

| Action | Method | Description |
| --- | --- | --- |
| [Get GDP by Industry Data](actions/get-gdp-by-industry-data.md) | GET | Retrieves GDP by industry data from the Bureau of Economic Analysis. |

### Iip Data

| Action | Method | Description |
| --- | --- | --- |
| [Get IIP Data](actions/get-iip-data.md) | GET | Retrieves IIP data from the Bureau of Economic Analysis. |

### Input-output Data

| Action | Method | Description |
| --- | --- | --- |
| [Get Input-Output Data](actions/get-input-output-data.md) | GET | Retrieves input-output data from the Bureau of Economic Analysis. |

### International Services Sta Data

| Action | Method | Description |
| --- | --- | --- |
| [Get International Services STA Data](actions/get-international-services-sta-data.md) | GET | Retrieves international services STA data from the Bureau of Economic Analysis. |

### International Services Trade Data

| Action | Method | Description |
| --- | --- | --- |
| [Get International Services Trade Data](actions/get-international-services-trade-data.md) | GET | Retrieves international services trade data from the Bureau of Economic Analysis. |

### Ita Data

| Action | Method | Description |
| --- | --- | --- |
| [Get ITA Data](actions/get-ita-data.md) | GET | Retrieves ITA data from the Bureau of Economic Analysis. |

### Mne Data

| Action | Method | Description |
| --- | --- | --- |
| [Get MNE Data](actions/get-mne-data.md) | GET | Retrieves MNE data from the Bureau of Economic Analysis. |

### Nipa Data

| Action | Method | Description |
| --- | --- | --- |
| [Get NIPA Data](actions/get-nipa-data.md) | GET | Retrieves NIPA data from the Bureau of Economic Analysis. |

### Nipa Underlying Detail Data

| Action | Method | Description |
| --- | --- | --- |
| [Get NIPA Underlying Detail Data](actions/get-nipa-underlying-detail-data.md) | GET | Retrieves NIPA underlying detail data from the Bureau of Economic Analysis. |

### Parameter

| Action | Method | Description |
| --- | --- | --- |
| [Get Parameter List](actions/get-parameter-list.md) | GET | Retrieves parameters for a Bureau of Economic Analysis dataset. |

### Parameter Value

| Action | Method | Description |
| --- | --- | --- |
| [Get Parameter Values](actions/get-parameter-values.md) | GET | Retrieves parameter values for a Bureau of Economic Analysis dataset. |

### Regional Data

| Action | Method | Description |
| --- | --- | --- |
| [Get Regional Data](actions/get-regional-data.md) | GET | Retrieves regional data from the Bureau of Economic Analysis. |

### Underlying Gdp By Industry Data

| Action | Method | Description |
| --- | --- | --- |
| [Get Underlying GDP by Industry Data](actions/get-underlying-gdp-by-industry-data.md) | GET | Retrieves underlying GDP by industry data from the Bureau of Economic Analysis. |

