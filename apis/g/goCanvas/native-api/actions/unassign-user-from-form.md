# Unassign User from Form with GoCanvas

## Endpoint

- **Method:** `DELETE`
- **Path:** `/forms/:formId/assigned_users/:userId`
- **Base URL:** `https://www.gocanvas.com/api/v3`
- **Official documentation:** [Unassign User from Form](https://api.gocanvas.com/api/v3/docs#unassign-user-from-form)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `number` | yes | — |
| `userId` | path | `number` | yes | — |
| `department_id` | body | `number` | no | Required when Departments are enabled for the GoCanvas company. |
