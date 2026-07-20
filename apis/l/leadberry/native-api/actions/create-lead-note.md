# Create Lead Note with Leadberry

## Endpoint

- **Method:** `POST`
- **Path:** `/data/saveNewNote`
- **Base URL:** `https://app.leadberry.com`
- **Official documentation:** [Create Lead Note](https://app.leadberry.com/js/dist/all.min.js?ver=20221103_1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `note` | body | `string` | yes | Leadberry note text to save for the current lead. |
| `isp` | body | `string` | yes | Leadberry ISP value for the current lead row. |
