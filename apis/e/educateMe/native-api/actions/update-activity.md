# Update Activity with EducateMe

Updates an existing activity in EducateMe.

## Endpoint

- **Method:** `POST`
- **Path:** `/activities/:activityId/update`
- **Base URL:** `https://api.educate-me.co`
- **Official documentation:** [Update Activity](https://edme.notion.site/API-integration-v0-2-ef33641eb7f24fa9a6efb969c1f2928f#7dd53470f51345a9bf6ee8da8f141fdc)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `activityId` | path | `string` | yes |
| `title` | body | `string` | yes |
| `mainHtml` | body | `string` | yes |
| `isDraft` | body | `boolean` | yes |
