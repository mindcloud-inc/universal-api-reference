# Get Company with Retently

Retrieves a company from Retently by ID or domain.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/companies/:companyIdOrDomain`
- **Base URL:** `https://app.retently.com`
- **Official documentation:** [Get Company](https://www.retently.com/api/#api-get-company-by-id-get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `companyIdOrDomain` | path | `string` | yes | Company ID or domain. |
