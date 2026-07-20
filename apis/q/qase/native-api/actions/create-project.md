# Create new project with Qase

Creates a new project in Qase.

## Endpoint

- **Method:** `POST`
- **Path:** `/project`
- **Base URL:** `https://api.qase.io/v1`
- **Official documentation:** [Create new project](https://developers.qase.io/reference/get-projects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | yes | Project title. |
| `code` | body | `string` | yes | Project code. Unique for team. Digits and special characters are not allowed. |
