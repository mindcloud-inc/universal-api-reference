# Add member absence with Status Hero

## Endpoint

- **Method:** `POST`
- **Path:** `/member_absences/:id`
- **Base URL:** `https://service.statushero.com/api/v1`
- **Official documentation:** [Add member absence](https://api.statushero.com/#add-member-absence)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The member ID or slug to mark absent. |
| `date` | body | `string` | yes | Absence date in YYYY-MM-DD format. |
