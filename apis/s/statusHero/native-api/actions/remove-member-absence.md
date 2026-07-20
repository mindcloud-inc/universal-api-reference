# Remove member absence with Status Hero

## Endpoint

- **Method:** `DELETE`
- **Path:** `/member_absences/:id/:date`
- **Base URL:** `https://service.statushero.com/api/v1`
- **Official documentation:** [Remove member absence](https://api.statushero.com/#remove-member-absence)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The member ID or slug for the absence to remove. |
| `date` | path | `string` | yes | Absence date in YYYY-MM-DD format. |
