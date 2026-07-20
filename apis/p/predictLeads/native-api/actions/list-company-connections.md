# List Company Connections with PredictLeads

Retrieves company connections from the PredictLeads API.

## Endpoint

- **Method:** `GET`
- **Path:** `/companies/:company_id_or_domain/connections`
- **Base URL:** `https://predictleads.com/api/v3`
- **Official documentation:** [List Company Connections](https://docs.predictleads.com/api_endpoints/connections_dataset/retrieve_company_s_connections)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_id_or_domain` | path | `string` | yes | Company's ID or domain. |
| `categories` | query | `string` | no | Comma-separated connection categories. |
| `first_seen_at_from` | query | `string` | no | Include connections first seen on or after this date. |
| `first_seen_at_until` | query | `string` | no | Include connections first seen on or before this date. |
