# List Popup Responses with Poper

Retrieves responses for a specific Poper popup.

## Endpoint

- **Method:** `POST`
- **Path:** `/popup/responses`
- **Base URL:** `https://api.poper.ai/general/v1`
- **Official documentation:** [List Popup Responses](https://support.poper.ai/en/articles/10095372-view-popup-responses)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `popup_id` | body | `string` | yes | The popup identifier whose responses you want to retrieve. |
