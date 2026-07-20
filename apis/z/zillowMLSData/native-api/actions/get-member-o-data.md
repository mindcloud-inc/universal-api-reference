# Get member (OData) with Zillow MLS Data

Retrieves a member record from Zillow MLS Data using OData.

## Endpoint

- **Method:** `GET`
- **Path:** `/OData/:dataset/Members(':memberKey')`
- **Base URL:** `https://api.bridgedataoutput.com/api/v2`
- **Official documentation:** [Get member (OData)](https://bridgedataoutput.com/docs/platform)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dataset` | path | `string` | yes | Bridge dataset code that contains the OData member. |
| `memberKey` | path | `string` | yes | OData member identifier from Bridge. |
