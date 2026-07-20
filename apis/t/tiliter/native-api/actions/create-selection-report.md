# Create Selection Report with Tiliter

Creates a selection report in the Tiliter Recognition API.

## Endpoint

- **Method:** `POST`
- **Path:** `/recognition/:recognition_id/selection_report`
- **Base URL:** `https://recognition.services.tiliter.com/v1/15`
- **Official documentation:** [Create Selection Report](https://developer.tiliter.com/reference/create_selection_report)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `recognition_id` | path | `string` | yes |
| `selectionMethod` | body | `string` | yes |
| `selectedProductId` | body | `string` | yes |
| `saleInfo` | body | `object` | yes |
| `selectionTime` | body | `date` | yes |
| `transactionId` | body | `string` | yes |
| `lineItemId` | body | `string` | yes |
