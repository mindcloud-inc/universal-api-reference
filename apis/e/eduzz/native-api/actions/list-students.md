# List Students with Eduzz

Retrieves students from Eduzz using the provided filters.

## Endpoint

- **Method:** `GET`
- **Path:** `/nutror/v1/students`
- **Base URL:** `https://api.eduzz.com`
- **Official documentation:** [List Students](https://developers.eduzz.com/reference/api/get-nutror-v1-students)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `string` | no | Id do aluno. |
| `email` | query | `string` | no | Email do aluno. |
