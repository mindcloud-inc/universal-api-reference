# Search Domain Emails with Hunter

## Endpoint

- **Method:** `GET`
- **Path:** `/domain-search`
- **Base URL:** `https://api.hunter.io/v2`
- **Official documentation:** [Search Domain Emails](https://hunter.io/api-documentation/v2#domain-search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | query | `string` | yes | Domain name to search, like hunter.io. |
| `company` | query | `string` | no | Company name to search when a domain is not provided. |
| `limit` | query | `number` | no | Maximum number of email addresses to return. |
| `offset` | query | `number` | no | Number of results to skip. |
| `type` | query | `string` | no | Filter to personal or generic email addresses. |
| `seniority` | query | `string` | no | Comma-delimited seniority filters. |
| `department` | query | `string` | no | Comma-delimited department filters. |
| `required_field` | query | `string` | no | Comma-delimited fields that must be present. |
| `verification_status` | query | `string` | no | Comma-delimited verification status filters. |
| `job_titles` | query | `string` | no | Comma-delimited job title filters. |
