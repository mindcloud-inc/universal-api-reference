# Generate Blank Bulk CSV with Xodo Sign

Retrieves a blank bulk sending CSV for a template in Xodo Sign.

## Endpoint

- **Method:** `GET`
- **Path:** `/template/:templateHash/bulk/csv/blank`
- **Base URL:** `https://api.eversign.com`
- **Official documentation:** [Generate Blank Bulk CSV](https://eversign.com/api/documentation/methods#get-bulk-sending-blank-csv)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `business_id` | query | `string` | yes | The Xodo Sign business ID that owns the template. |
| `templateHash` | path | `string` | yes | The template hash to use for bulk sending CSV generation. |
