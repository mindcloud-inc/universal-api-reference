# Create Mid Call Tool with Famulor AI - Voice Agent

Creates a new mid-call tool in Famulor.

## Endpoint

- **Method:** `POST`
- **Path:** `/user/tools`
- **Base URL:** `https://app.famulor.de/api`
- **Official documentation:** [Create Mid Call Tool](https://docs.famulor.io/en/api-reference/mid-call-tools/create-tool)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | yes | Explanation of when and how the assistant should use the tool. |
| `endpoint` | body | `string` | yes | External API endpoint URL for the tool. |
| `method` | body | `string` | yes | HTTP method the tool should use. |
| `name` | body | `string` | yes | Mid-call tool identifier. |
