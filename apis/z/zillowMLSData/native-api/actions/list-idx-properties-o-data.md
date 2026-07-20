# List IDX properties (OData) with Zillow MLS Data

Retrieves IDX property records from Zillow MLS Data using OData.

## Endpoint

- **Method:** `GET`
- **Path:** `/OData/:dataset/idx/Properties`
- **Base URL:** `https://api.bridgedataoutput.com/api/v2`
- **Official documentation:** [List IDX properties (OData)](https://bridgedataoutput.com/docs/platform)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dataset` | path | `string` | yes | Bridge dataset code that scopes the OData IDX properties query. |
