# Add User to Department with GoCanvas

## Endpoint

- **Method:** `POST`
- **Path:** `/departments/:departmentId/users`
- **Base URL:** `https://www.gocanvas.com/api/v3`
- **Official documentation:** [Add User to Department](https://api.gocanvas.com/api/v3/docs#add-a-user-to-a-department)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `departmentId` | path | `number` | yes | — |
| `user_id` | body | `number` | yes | — |
| `department_role` | body | `list<string>` | yes | Accepted values: `department_admin`, `department_designer`, `department_dispatcher`, `department_reporter`, `department_user`. |
