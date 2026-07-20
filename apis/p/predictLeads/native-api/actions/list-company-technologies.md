# List Company Technologies with PredictLeads

Retrieves technologies used by a PredictLeads company.

## Endpoint

- **Method:** `GET`
- **Path:** `/companies/:company_id_or_domain/technology_detections`
- **Base URL:** `https://predictleads.com/api/v3`
- **Official documentation:** [List Company Technologies](https://docs.predictleads.com/api_endpoints/technology_detections_dataset/retrieve_technologies_used_by_specific_company)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_id_or_domain` | path | `string` | yes | Company ID or domain. |
| `first_seen_at_from` | query | `date` | no | Only return technology detections first seen after the given date (ISO 8601). |
| `first_seen_at_until` | query | `date` | no | Only return technology detections first seen before the given date (ISO 8601). |
| `last_seen_at_from` | query | `date` | no | Only return technology detections last seen after the given date (ISO 8601). |
| `last_seen_at_until` | query | `date` | no | Only return technology detections last seen before the given date (ISO 8601). |
| `page` | query | `number` | no | Page number of shown items. |
| `limit` | query | `number` | no | Limit the number of shown items per page. |
