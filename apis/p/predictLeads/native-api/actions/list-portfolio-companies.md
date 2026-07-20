# List Portfolio Companies with PredictLeads

Retrieves portfolio companies from the PredictLeads API.

## Endpoint

- **Method:** `GET`
- **Path:** `/discover/portfolio_companies/connections`
- **Base URL:** `https://predictleads.com/api/v3`
- **Official documentation:** [List Portfolio Companies](https://docs.predictleads.com/api_endpoints/connections_dataset/retrieve_portfolio_companies)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `first_seen_at_from` | query | `string` | no | Include portfolio-company connections first seen on or after this date. |
| `first_seen_at_until` | query | `string` | no | Include portfolio-company connections first seen on or before this date. |
| `last_seen_at_from` | query | `string` | no | Include portfolio-company connections last seen on or after this date. |
| `last_seen_at_until` | query | `string` | no | Include portfolio-company connections last seen on or before this date. |
