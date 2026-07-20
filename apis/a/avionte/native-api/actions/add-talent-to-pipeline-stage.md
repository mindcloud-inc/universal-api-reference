# Add Talent to Pipeline Stage with Avionte

## Endpoint

- **Method:** `POST`
- **Path:** `front-office/v1/pipeline/talent-stage/add`
- **Base URL:** `https://api.avionte.com/`
- **Official documentation:** [Add Talent to Pipeline Stage](https://developer.avionte.com/reference/addtalentpipelinestage)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `jobActivityName` | body | `string` | yes |
| `jobId` | body | `string` | yes |
| `talentId` | body | `string` | yes |
| `stageType` | body | `string` | yes |
| `stagedDate` | body | `string` | yes |
| `jobActivityDate` | body | `string` | yes |
