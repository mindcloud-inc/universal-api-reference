# Retrieve Form Report with GoCanvas

## Endpoint

- **Method:** `GET`
- **Path:** `/forms/:formId/reports/:reportId`
- **Base URL:** `https://www.gocanvas.com/api/v3`
- **Official documentation:** [Retrieve Form Report](https://api.gocanvas.com/api/v3/docs#single-report-by-form)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `number` | yes | — |
| `reportId` | path | `number` | yes | Use -2 for a Quick Start or Designer PDF when returned by List Form Reports. |
