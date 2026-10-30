# Retrieve Form with GoCanvas

## Endpoint

- **Method:** `GET`
- **Path:** `/forms/:formId`
- **Base URL:** `https://www.gocanvas.com/api/v3`
- **Official documentation:** [Retrieve Form](https://api.gocanvas.com/api/v3/docs#retrieve-a-form)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `number` | yes | — |
| `format` | query | `list` | no | The response format. Defaults to nested. Accepted values: `flat`, `metadata`, `minimal`, `nested`. |
