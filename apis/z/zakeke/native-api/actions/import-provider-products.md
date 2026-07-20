# Import Provider Products with Zakeke

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/providerproducts/import`
- **Base URL:** `https://api.zakeke.com`
- **Official documentation:** [Import Provider Products](https://docs.zakeke.com/docs/API/Integration/Connecting-Product/CSV-method#3-second-step-check-the-import-status)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `canvasBorders[]` | body | `array<object>` | no | Optional provider canvas borders. |
| `multiCanvasSettings[]` | body | `array<object>` | no | Optional provider multi-canvas settings. |
| `product3DSettings[]` | body | `array<object>` | no | Optional provider 3D settings. |
| `products[]` | body | `array<object>` | no | Provider product list to import. |
| `productTypes[]` | body | `array<object>` | no | Provider product types and print constraints. |
| `resizableSettings[]` | body | `array<object>` | no | Optional provider resizable settings. |
| `version` | body | `string` | no | Optional payload version. |
