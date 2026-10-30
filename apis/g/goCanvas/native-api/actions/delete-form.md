# Delete Form with GoCanvas

## Endpoint

- **Method:** `DELETE`
- **Path:** `/forms/:formId`
- **Base URL:** `https://www.gocanvas.com/api/v3`
- **Official documentation:** [Delete Form](https://api.gocanvas.com/api/v3/docs#delete-a-form)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `number` | yes | — |
| `hard_delete` | query | `boolean` | no | Permanently delete the form and associated data. Omit for soft deletion. |
