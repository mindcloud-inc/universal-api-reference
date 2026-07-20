# Get property (OData) with Bridge Interactive Platform

Retrieves a property from Bridge Interactive Platform.

## Endpoint

- **Method:** `GET`
- **Path:** `/OData/:dataset/Property(':ListingKey')`
- **Base URL:** `https://api.bridgedataoutput.com/api/v2`
- **Official documentation:** [Get property (OData)](https://bridgedataoutput.com/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dataset` | path | `string` | yes | Bridge dataset code. This tenant was validated against dataset test. |
| `ListingKey` | path | `string` | yes | OData property identifier from Bridge. |
