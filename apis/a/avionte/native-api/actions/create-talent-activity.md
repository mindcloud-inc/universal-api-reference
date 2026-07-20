# Create Talent Activity with Avionte

## Endpoint

- **Method:** `POST`
- **Path:** `front-office/v1/talent/:talentId/activity`
- **Base URL:** `https://api.avionte.com/`
- **Official documentation:** [Create Talent Activity](https://developer.avionte.com/reference/createtalentactivity)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `talentId` | path | `string` | yes |
| `notes` | body | `string` | yes |
| `name` | body | `string` | no |
| `typeId` | body | `number` | yes |
