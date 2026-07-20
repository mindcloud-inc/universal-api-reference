# Get office (OData) with Zillow MLS Data

Retrieves an office record from Zillow MLS Data using OData.

## Endpoint

- **Method:** `GET`
- **Path:** `/OData/:dataset/Offices(':officeKey')`
- **Base URL:** `https://api.bridgedataoutput.com/api/v2`
- **Official documentation:** [Get office (OData)](https://bridgedataoutput.com/docs/platform)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dataset` | path | `string` | yes | Bridge dataset code that contains the OData office. |
| `officeKey` | path | `string` | yes | OData office identifier from Bridge. |
