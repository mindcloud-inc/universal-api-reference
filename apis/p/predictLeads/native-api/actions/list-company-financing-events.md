# List Company Financing Events with PredictLeads

Retrieves financing events for a PredictLeads company.

## Endpoint

- **Method:** `GET`
- **Path:** `/companies/:company_id_or_domain/financing_events`
- **Base URL:** `https://predictleads.com/api/v3`
- **Official documentation:** [List Company Financing Events](https://docs.predictleads.com/api_endpoints/financing_events_dataset/retrieve_company_s_financing_events)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_id_or_domain` | path | `string` | yes | Company's ID or domain. |
| `first_seen_at_from` | query | `string` | no | Include financing events first seen on or after this date. |
| `first_seen_at_until` | query | `string` | no | Include financing events first seen on or before this date. |
