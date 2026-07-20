# List Skills with Sertifier

Finds skills in Sertifier by search filters.

## Endpoint

- **Method:** `POST`
- **Path:** `/detail/searchSkills`
- **Base URL:** `https://b2b.sertifier.com`
- **Official documentation:** [List Skills](https://sertifier.docs.apiary.io/reference/detail/search-skills)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `searchTerm` | body | `string` | no | Filter skills by matching title text. |
| `language` | body | `string` | yes | Skill language code. Sertifier supports en or tr. |
