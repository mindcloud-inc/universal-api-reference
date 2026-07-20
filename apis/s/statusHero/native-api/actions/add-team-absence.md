# Add team absence with Status Hero

## Endpoint

- **Method:** `POST`
- **Path:** `/team_absences`
- **Base URL:** `https://service.statushero.com/api/v1`
- **Official documentation:** [Add team absence](https://api.statushero.com/#add-team-absence)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date` | body | `string` | yes | Team-wide absence date in YYYY-MM-DD format. |
