# Process Return with Loop Returns

Process a return in Loop based on the return ID. Processing a return will archive it in Loop and fulfill any remaining outcomes, such as placing exchange orders or creating gift cards.

## Endpoint

- **Method:** `POST`
- **Path:** `https://api.loopreturns.com/api/v1/warehouse/return/{{return_id}}/process`
- **Base URL:** `https://api.loopreturns.com/api/v1`
- **Official documentation:** [Process Return](https://docs.loopreturns.com/api-reference/latest/return-actions/process-return)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `return_id` | path | `string` | yes |
