# Update Mid Call Tool with Famulor AI - Voice Agent

Updates an existing mid-call tool in Famulor.

## Endpoint

- **Method:** `PUT`
- **Path:** `/user/tools/:id`
- **Base URL:** `https://app.famulor.de/api`
- **Official documentation:** [Update Mid Call Tool](https://docs.famulor.io/en/api-reference/mid-call-tools/update-tool)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | no | Explanation of when and how the assistant should use the tool. |
| `endpoint` | body | `string` | no | External API endpoint URL for the tool. |
| `id` | path | `number` | yes | Famulor mid-call tool ID. |
| `method` | body | `string` | no | HTTP method the tool should use. |
| `name` | body | `string` | no | Mid-call tool identifier. |
