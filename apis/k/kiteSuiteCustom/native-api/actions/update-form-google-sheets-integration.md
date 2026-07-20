# Update Form Google Sheets Integration with Kite Suite

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v1/form/integration/google-sheet/:id`
- **Base URL:** `https://api.kitesuite.com`
- **Official documentation:** [Update Form Google Sheets Integration](https://api.kitesuite.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `object` | yes | Request body |
| `id` | path | `string` | yes | ID of the Google Sheets integration to update. |
| `selectedAdvancedOptions[]` | body | `array` | yes | Updated array of advanced options to include. |
| `selectedFields[]` | body | `array` | yes | Updated array of form element IDs to include. |
