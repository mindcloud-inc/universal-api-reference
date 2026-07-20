# Get property (OData) with Zillow MLS Data

Retrieves a property record from Zillow MLS Data using OData.

## Endpoint

- **Method:** `GET`
- **Path:** `/OData/:dataset/Properties(':listingKey')`
- **Base URL:** `https://api.bridgedataoutput.com/api/v2`
- **Official documentation:** [Get property (OData)](https://bridgedataoutput.com/docs/platform)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dataset` | path | `string` | yes | Bridge dataset code that contains the OData property. |
| `listingKey` | path | `string` | yes | OData property identifier from Bridge. |
