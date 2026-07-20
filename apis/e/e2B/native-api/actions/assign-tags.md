# Assign Tags with E2B

Assigns tags to a template build in E2B.

## Endpoint

- **Method:** `POST`
- **Path:** `/templates/tags`
- **Base URL:** `https://api.e2b.app`
- **Official documentation:** [Assign Tags](https://e2b.dev/docs/api-reference/tags/assign-tags)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tags[]` | body | `array<string>` | yes | Tags to assign to the template. |
| `target` | body | `string` | yes | Target template in name:tag format. |
