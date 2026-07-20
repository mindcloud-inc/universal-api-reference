# Collect Clean Company By Identifier with Coresignal

Collects a clean company from Coresignal by identifier.

## Endpoint

- **Method:** `GET`
- **Path:** `/company_clean/collect/:companyIdentifier`
- **Base URL:** `https://api.coresignal.com/cdapi/v2`
- **Official documentation:** [Collect Clean Company By Identifier](https://docs.coresignal.com/company-api/clean-company-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `companyIdentifier` | path | `string` | yes | LinkedIn company URL or shorthand name accepted by the Clean Company collect endpoint. |
