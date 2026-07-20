# Import Provider Product Templates with Zakeke

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/providerproducts/importTemplates`
- **Base URL:** `https://api.zakeke.com`
- **Official documentation:** [Import Provider Product Templates](https://api-reference.zakeke.com/docs)

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
| `forceDelete` | query | `boolean` | no | Delete previous templates before import. |
| `multiCanvasSettings[]` | body | `array<object>` | no | Optional provider multi-canvas settings. |
| `product3DSettings[]` | body | `array<object>` | no | Optional provider 3D settings. |
| `products[]` | body | `array<object>` | no | Provider product list to import as templates. |
| `productTypes[]` | body | `array<object>` | no | Provider product types and print constraints. |
| `resizableSettings[]` | body | `array<object>` | no | Optional provider resizable settings. |
| `version` | body | `string` | no | Optional payload version. |
