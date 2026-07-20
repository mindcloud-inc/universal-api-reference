# Update Customer Notes with Dukaan

Updates customer notes in Dukaan.

## Endpoint

- **Method:** `PATCH`
- **Path:** `api/order/seller/:storeLeadId/update-storelead-notes/`
- **Base URL:** `https://api.mydukaan.io`
- **Official documentation:** [Update Customer Notes](https://documenter.getpostman.com/view/25389466/2s9Yynk3f7)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `storeLeadId` | path | `number` | yes | Dukaan store lead/customer ID. |
| `notes` | body | `string` | yes | Customer note text. |
