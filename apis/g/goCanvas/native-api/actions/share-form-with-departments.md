# Share Form with Departments with GoCanvas

## Endpoint

- **Method:** `POST`
- **Path:** `/forms/:formId/shared_departments`
- **Base URL:** `https://www.gocanvas.com/api/v3`
- **Official documentation:** [Share Form with Departments](https://api.gocanvas.com/api/v3/docs#share-form-with-departments)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `number` | yes | — |
| `department_ids[]` | body | `array<number>` | yes | Department IDs to share with, up to 50. |
