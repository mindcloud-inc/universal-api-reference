# Create Talent Tag with Avionte

## Endpoint

- **Method:** `POST`
- **Path:** `front-office/v1/talent/:talentId/talenttag`
- **Base URL:** `https://api.avionte.com/`
- **Official documentation:** [Create Talent Tag](https://developer.avionte.com/reference/addtalenttag)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `tag` | body | `string` | yes |
| `talentId` | path | `string` | yes |
| `detail` | body | `string` | no |
| `expirationDate` | body | `date` | no |
| `talentId` | body | `number` | yes |
