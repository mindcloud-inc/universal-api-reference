# Find Manager with The Org

Finds a manager in The Org by email or LinkedIn URL.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1.1/companies/org-chart/managers`
- **Base URL:** `https://api.theorg.com`
- **Official documentation:** [Find Manager](https://developers.theorg.com/api/endpoints/company-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | query | `string` | no | Email address of the person. |
| `linkedInUrl` | query | `string` | no | LinkedIn profile URL of the person. |
