# Get Domain by Company Name with Company URL Finder

Finds a company's domain in Company URL Finder by company name.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/services/name_to_domain`
- **Base URL:** `https://api.companyurlfinder.com`
- **Official documentation:** [Get Domain by Company Name](https://apidocs.companyurlfinder.com/apis/company-name-to-domain)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_name` | body | `string` | yes | Company name. |
| `country_code` | body | `string` | yes | Two-letter country code. When set, results are limited to that country. |
