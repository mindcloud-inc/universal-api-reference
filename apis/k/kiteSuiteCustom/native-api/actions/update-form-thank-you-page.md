# Update Form Thank You Page with Kite Suite

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v1/form-ty/:id`
- **Base URL:** `https://api.kitesuite.com`
- **Official documentation:** [Update Form Thank You Page](https://api.kitesuite.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Form Thank You Page ID |
| `body` | body | `object` | yes | Request body |
| `button` | body | `object` | yes | — |
| `logo` | body | `string` | yes | URL or ID of the logo image |
| `logoZoom` | body | `number` | yes | Zoom level for the logo |
| `text` | body | `string` | yes | Thank you message text |
| `buttonAlignment` | body | `string` | yes | Alignment of the button |
| `nextSubmission` | body | `boolean` | yes | Whether to allow next submission |
| `layoutDirection` | body | `string` | yes | Direction of the layout |
