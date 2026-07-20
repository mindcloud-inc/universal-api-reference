# List Pipelines with HubSpot

Retrieves pipelines from HubSpot.

## Endpoint

- **Method:** `GET`
- **Path:** `crm/v3/pipelines/:objectType`
- **Base URL:** `https://api.hubapi.com`
- **API:** REST - Query Pagination
- **Official documentation:** [List Pipelines](https://developers.hubspot.com/docs/api-reference/crm-pipelines-v3/pipelines/get-crm-v3-pipelines-objectType)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `objectType` | path | `string` | yes | The object type whose pipelines to retrieve, such as deals or tickets. |
