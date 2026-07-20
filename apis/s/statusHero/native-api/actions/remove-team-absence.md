# Remove team absence with Status Hero

## Endpoint

- **Method:** `DELETE`
- **Path:** `/team_absences/:date`
- **Base URL:** `https://service.statushero.com/api/v1`
- **Official documentation:** [Remove team absence](https://api.statushero.com/#remove-team-absence)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date` | path | `string` | yes | Team-wide absence date in YYYY-MM-DD format. |
