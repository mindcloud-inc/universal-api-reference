# Create Proposal with MILKEE

Creates a new proposal in MILKEE.

## Endpoint

- **Method:** `POST`
- **Path:** `/companies/:companyId/proposals`
- **Base URL:** `https://app.milkee.ch/api/v2`
- **Official documentation:** [Create Proposal](https://apidocs.milkee.ch/api/resources/proposals.html#neue-offerte-erstellen)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company` | path | `string` | yes | The numeric MILKEE company ID used in the request path. |
| `customer_id` | body | `number` | yes | Customer ID for the proposal. |
| `date` | body | `string` | no | Proposal date. |
| `lang` | body | `string` | no | Document language: de, en, fr, or it. |
| `positions` | body | `string` | no | Proposal positions as a JSON string. |
| `remarks` | body | `string` | no | Bottom remarks. |
| `tax_rate_id` | body | `number` | no | Tax rate ID. |
| `title` | body | `string` | no | Proposal title. |
| `valid_until` | body | `string` | no | Proposal expiration date. |
