# List Technology Companies with PredictLeads

Retrieves companies using a technology from PredictLeads.

## Endpoint

- **Method:** `GET`
- **Path:** `/discover/technologies/:technology_id_or_fuzzy_name/technology_detections`
- **Base URL:** `https://predictleads.com/api/v3`
- **Official documentation:** [List Technology Companies](https://docs.predictleads.com/api_endpoints/technology_detections_dataset/retrieve_companies_using_specific_technology_id_or_fuzzy_name)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `technology_id_or_fuzzy_name` | path | `string` | yes | Technology ID or fuzzy name. |
| `first_seen_at_from` | query | `date` | no | Only return technology detections first seen after the given date (ISO 8601). |
| `first_seen_at_until` | query | `date` | no | Only return technology detections first seen before the given date (ISO 8601). |
| `last_seen_at_from` | query | `date` | no | Only return technology detections last seen after the given date (ISO 8601). |
| `last_seen_at_until` | query | `date` | no | Only return technology detections last seen before the given date (ISO 8601). |
| `page` | query | `number` | no | Page number of shown items. |
| `limit` | query | `number` | no | Limit the number of shown items per page. |
