# List Fields By Service with Environmental Protection Agency

Retrieves field definitions for a selected EPA AQS service.

## Endpoint

- **Method:** `GET`
- **Path:** `/metaData/fieldsByService`
- **Base URL:** `https://aqs.epa.gov/data/api`
- **Official documentation:** [List Fields By Service](https://aqs.epa.gov/aqsweb/documents/data_api.html#metadata)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `service` | query | `string` | yes | EPA AQS service name to return field definitions for, such as sampleData or list. |
