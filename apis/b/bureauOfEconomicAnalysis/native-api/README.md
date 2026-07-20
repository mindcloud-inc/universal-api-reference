# Bureau of Economic Analysis: Native API Reference

A consolidated summary of Bureau of Economic Analysis's API configuration and 17 documented operations, with links to official documentation.

- **Official docs:** https://apps.bea.gov/api/_pdf/bea_web_service_api_user_guide.pdf
- **API base URL:** `https://apps.bea.gov/api`

## Authentication

### BEA API Key

BEA UserID API key used for API requests.

### Credentials

- **BEA UserID:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://apps.bea.gov/api/_pdf/bea_web_service_api_user_guide.pdf)

## API conventions

Responses from this API use JSON. Response data is read from `BEAAPI.Results`.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (17 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get API Dataset Metadata](actions/get-api-dataset-metadata.md) | `GET /data` | [docs](https://apps.bea.gov/api/_pdf/bea_web_service_api_user_guide.pdf) |
| [Get Dataset List](actions/get-dataset-list.md) | `GET /data` | [docs](https://apps.bea.gov/api/_pdf/bea_web_service_api_user_guide.pdf) |
| [Get Filtered Parameter Values](actions/get-filtered-parameter-values.md) | `GET /data` | [docs](https://apps.bea.gov/api/_pdf/bea_web_service_api_user_guide.pdf) |
| [Get Fixed Assets Data](actions/get-fixed-assets-data.md) | `GET /data` | [docs](https://apps.bea.gov/api/_pdf/bea_web_service_api_user_guide.pdf) |
| [Get GDP by Industry Data](actions/get-gdp-by-industry-data.md) | `GET /data` | [docs](https://apps.bea.gov/api/_pdf/bea_web_service_api_user_guide.pdf) |
| [Get IIP Data](actions/get-iip-data.md) | `GET /data` | [docs](https://apps.bea.gov/api/_pdf/bea_web_service_api_user_guide.pdf) |
| [Get Input-Output Data](actions/get-input-output-data.md) | `GET /data` | [docs](https://apps.bea.gov/api/_pdf/bea_web_service_api_user_guide.pdf) |
| [Get International Services STA Data](actions/get-international-services-sta-data.md) | `GET /data` | [docs](https://apps.bea.gov/api/_pdf/bea_web_service_api_user_guide.pdf) |
| [Get International Services Trade Data](actions/get-international-services-trade-data.md) | `GET /data` | [docs](https://apps.bea.gov/api/_pdf/bea_web_service_api_user_guide.pdf) |
| [Get ITA Data](actions/get-ita-data.md) | `GET /data` | [docs](https://apps.bea.gov/api/_pdf/bea_web_service_api_user_guide.pdf) |
| [Get MNE Data](actions/get-mne-data.md) | `GET /data` | [docs](https://apps.bea.gov/api/_pdf/bea_web_service_api_user_guide.pdf) |
| [Get NIPA Data](actions/get-nipa-data.md) | `GET /data` | [docs](https://apps.bea.gov/api/_pdf/bea_web_service_api_user_guide.pdf) |
| [Get NIPA Underlying Detail Data](actions/get-nipa-underlying-detail-data.md) | `GET /data` | [docs](https://apps.bea.gov/api/_pdf/bea_web_service_api_user_guide.pdf) |
| [Get Parameter List](actions/get-parameter-list.md) | `GET /data` | [docs](https://apps.bea.gov/api/_pdf/bea_web_service_api_user_guide.pdf) |
| [Get Parameter Values](actions/get-parameter-values.md) | `GET /data` | [docs](https://apps.bea.gov/api/_pdf/bea_web_service_api_user_guide.pdf) |
| [Get Regional Data](actions/get-regional-data.md) | `GET /data` | [docs](https://apps.bea.gov/api/_pdf/bea_web_service_api_user_guide.pdf) |
| [Get Underlying GDP by Industry Data](actions/get-underlying-gdp-by-industry-data.md) | `GET /data` | [docs](https://apps.bea.gov/api/_pdf/bea_web_service_api_user_guide.pdf) |
