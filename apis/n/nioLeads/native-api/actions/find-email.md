# Find Email with NioLeads

Finds a business email in NioLeads by name and domain.

## Endpoint

- **Method:** `POST`
- **Path:** `/find_email`
- **Base URL:** `https://v2.nioleads.com/api/openapi`
- **Official documentation:** [Find Email](https://nioleads.com/apidoc/#email-finder)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `firstname` | body | `string` | yes | Person's first name |
| `lastname` | body | `string` | yes | Person's last name |
| `domainOrCompany` | body | `string` | yes | Email domain or company name |
