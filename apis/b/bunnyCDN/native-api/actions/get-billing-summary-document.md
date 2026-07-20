# Get Billing Summary Document with BunnyCDN

Retrieves a BunnyCDN billing summary PDF.

## Endpoint

- **Method:** `GET`
- **Path:** `/billing/summary/:billingRecordId/pdf`
- **Base URL:** `https://api.bunny.net`
- **Official documentation:** [Get Billing Summary Document](https://docs.bunny.net/reference/bunnynet-api-overview)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `billingRecordId` | path | `string` | yes | The Bunny billing summary record ID. |
