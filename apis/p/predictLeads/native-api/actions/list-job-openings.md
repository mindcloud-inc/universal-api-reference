# List Job Openings with PredictLeads

Retrieves job openings from the PredictLeads API.

## Endpoint

- **Method:** `GET`
- **Path:** `/discover/job_openings`
- **Base URL:** `https://predictleads.com/api/v3`
- **Official documentation:** [List Job Openings](https://docs.predictleads.com/api_endpoints/job_openings_dataset/retrieve_a_list_of_job_openings)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `location` | query | `string` | no | Filter job openings by location. |
| `onet_codes` | query | `string` | no | Comma-separated ONET occupation codes. |
