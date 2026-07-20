# Get Transfer with Fintoc

Retrieves a transfer from Fintoc.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/transfers/:transfer_id`
- **Base URL:** `https://api.fintoc.com`
- **Official documentation:** [Get Transfer](https://docs.fintoc.com/reference/retrieve-transfer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `transfer_id` | path | `string` | yes | Transfer identifier (for example `tr_...`). |
