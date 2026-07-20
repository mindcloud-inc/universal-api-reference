# Create Changelog with Productlane

Creates a new changelog in Productlane.

## Endpoint

- **Method:** `POST`
- **Path:** `/changelogs`
- **Base URL:** `https://productlane.com/api/v1`
- **Official documentation:** [Create Changelog](https://productlane.mintlify.dev/docs/api/changelogs/create-changelog)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `title` | body | `string` | yes |
| `content` | body | `string` | yes |
| `date` | body | `date` | no |
| `published` | body | `boolean` | no |
| `language` | body | `string` | no |
| `tagIds[]` | body | `array<string>` | no |
