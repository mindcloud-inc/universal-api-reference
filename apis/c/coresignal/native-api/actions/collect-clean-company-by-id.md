# Collect Clean Company By ID with Coresignal

Collects a clean company from Coresignal by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/company_clean/collect/:companyId`
- **Base URL:** `https://api.coresignal.com/cdapi/v2`
- **Official documentation:** [Collect Clean Company By ID](https://docs.coresignal.com/company-api/clean-company-api/endpoints/collect-company)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `companyId` | path | `number` | yes | Coresignal clean company identifier returned by preview or bulk search results. |
