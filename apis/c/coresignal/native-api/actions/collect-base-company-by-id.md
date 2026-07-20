# Collect Base Company By ID with Coresignal

Collects a base company from Coresignal by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/company_base/collect/:companyId`
- **Base URL:** `https://api.coresignal.com/cdapi/v2`
- **Official documentation:** [Collect Base Company By ID](https://docs.coresignal.com/company-api/base-company-api/endpoints/collect-company)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `companyId` | path | `number` | yes | Coresignal company identifier returned by preview or bulk search results. |
