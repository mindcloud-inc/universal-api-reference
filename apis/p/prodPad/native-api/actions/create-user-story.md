# Create User Story with ProdPad

Creates a new user story in ProdPad.

## Endpoint

- **Method:** `POST`
- **Path:** `/userstories`
- **Base URL:** `https://api.prodpad.com/v1`
- **Official documentation:** [Create User Story](https://app.swaggerhub.com/apis-docs/ProdPad/prodpad/1.1.4#/Ideas/PostUserStories)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `title` | body | `string` | no |
| `story` | body | `string` | yes |
| `acceptance_criteria` | body | `string` | no |
| `idea.id` | body | `string` | yes |
| `status.id` | body | `string` | no |
