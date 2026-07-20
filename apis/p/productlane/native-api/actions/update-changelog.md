# Update Changelog with Productlane

Updates an existing changelog in Productlane.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/changelogs/:id`
- **Base URL:** `https://productlane.com/api/v1`
- **Official documentation:** [Update Changelog](https://productlane.mintlify.dev/docs/api/changelogs/update-changelog)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `title` | body | `string` | no |
| `content` | body | `string` | no |
| `date` | body | `date` | no |
| `published` | body | `boolean` | no |
| `archived` | body | `boolean` | no |
| `tagIds[]` | body | `array<string>` | no |
