# Validate Schema with Rossum

Validates a schema in Rossum.

## Endpoint

- **Method:** `POST`
- **Path:** `/schemas/validate`
- **Base URL:** `https://mindcloud.rossum.app/api/v1`
- **Official documentation:** [Validate Schema](https://rossum.app/api/docs/openapi/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `content` | body | `list<object>` | yes | Rossum schema content definition. |
