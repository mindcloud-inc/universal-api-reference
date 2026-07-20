# List IDX field rules (OData) with Zillow MLS Data

Retrieves IDX field rules from Zillow MLS Data using OData.

## Endpoint

- **Method:** `GET`
- **Path:** `/OData/:dataset/idx/Field`
- **Base URL:** `https://api.bridgedataoutput.com/api/v2`
- **Official documentation:** [List IDX field rules (OData)](https://bridgedataoutput.com/docs/platform)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dataset` | path | `string` | yes | Bridge dataset code that scopes the OData IDX field rules query. |
