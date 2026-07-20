# Create Tag with EducateMe

Creates a new tag in EducateMe.

## Endpoint

- **Method:** `POST`
- **Path:** `/tags`
- **Base URL:** `https://api.educate-me.co`
- **Official documentation:** [Create Tag](https://edme.notion.site/API-integration-v0-2-ef33641eb7f24fa9a6efb969c1f2928f#2bf447e2efaa80589d3fe71414c60fff)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | yes | Tag title. |
| `category` | body | `string` | yes | Tag category. Allowed values: LOCATION, OTHER, ROLE, DEPARTMENT, TEAM, FUNCTION, UNIT, PROBATION. Accepted values: `0`, `1`, `2`, `3`, `4`, `5`, `6`, `7`. |
