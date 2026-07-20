# Create Bulk Job with Xodo Sign

Creates a new bulk job in Xodo Sign.

## Endpoint

- **Method:** `POST`
- **Path:** `/template/:templateHash/bulk/job`
- **Base URL:** `https://api.eversign.com`
- **Official documentation:** [Create Bulk Job](https://eversign.com/api/documentation/methods#create-bulk-job)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `business_id` | query | `string` | yes | Business ID to scope the bulk job request. |
| `templateHash` | path | `string` | yes | Template hash used for the bulk sending job. |
| `[]` | body | `array<array>` | yes | Two-dimensional array payload for the bulk job. The first row is the header row and each following row is one bulk-send record. |
