# Assign User to Form with GoCanvas

## Endpoint

- **Method:** `POST`
- **Path:** `/forms/:formId/assigned_users`
- **Base URL:** `https://www.gocanvas.com/api/v3`
- **Official documentation:** [Assign User to Form](https://api.gocanvas.com/api/v3/docs#assign-user-to-form)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `number` | yes | — |
| `user_id` | body | `number` | yes | — |
| `department_id` | body | `number` | no | Required when Departments are enabled for the GoCanvas company. |
