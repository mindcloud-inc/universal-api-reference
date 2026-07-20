# Create Refund with PayWhirl

Creates a refund for a PayWhirl charge.

## Endpoint

- **Method:** `POST`
- **Path:** `/refund/charge/{id}`
- **Base URL:** `https://api.paywhirl.com`
- **Official documentation:** [Create Refund](https://api.paywhirl.com/#charges)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The PayWhirl charge ID. |
