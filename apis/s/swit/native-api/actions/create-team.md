# Create Team with Swit

Creates a new team in Swit.

## Endpoint

- **Method:** `POST`
- **Path:** `team.create`
- **Base URL:** `https://openapi.swit.io`
- **Official documentation:** [Create Team](https://tech-support.swit.io/books/swit-java-development-guide/page/3fe94)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Name of the team to create. |
| `parent_id` | body | `number` | yes | Parent team ID. Use 0 for a root team. |
| `reference` | body | `string` | no | Optional external reference for the team. |
