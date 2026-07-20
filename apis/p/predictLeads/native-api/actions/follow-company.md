# Follow Company with PredictLeads

Follows a company in the PredictLeads API.

## Endpoint

- **Method:** `POST`
- **Path:** `/companies/:company_id_or_domain/follow`
- **Base URL:** `https://predictleads.com/api/v3`
- **Official documentation:** [Follow Company](https://docs.predictleads.com/api_endpoints/follow_companies/follow_the_company)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_id_or_domain` | path | `string` | yes | Company ID or domain. |
| `custom_company_identifier` | query | `string` | no | Use your custom company identifier if you want it stored with the follow. |
