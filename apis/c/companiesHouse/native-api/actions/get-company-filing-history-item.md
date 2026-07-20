# Get Company Filing History Item with Companies House

Retrieves a company filing history item from Companies House.

## Endpoint

- **Method:** `GET`
- **Path:** `/company/:company_number/filing-history/:transaction_id`
- **Base URL:** `https://api.company-information.service.gov.uk`
- **Official documentation:** [Get Company Filing History Item](https://developer-specs.company-information.service.gov.uk/companies-house-public-data-api/reference/filing-history/list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_number` | path | `string` | yes | The company number. |
| `transaction_id` | path | `string` | yes | The filing transaction ID. |
